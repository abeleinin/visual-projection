# Projection Experiment Data

This repository is open sources a dataset gathered from cognitive science research on visual projection. We provide data from 40 participants solving this [modified visual paterns test](https://projection-experiment.vercel.app/).

## Table of Contents

- [Method](#method)
- [Results](#results)
- [Data](#data)

### **Figure 1.** Modified visual patterns test timeline

<img src="./figs/experiment_timeline.png" alt="Visual projection experiment timeline" height="500">

> **Note:** Trial timeline illustrating the sequence of visual stimuli and masking conditions. Participants first view the initial Board State for 1000 ms, followed by the Stimulus for 2000 ms. Subsequently, either no mask is presented (as shown on the left side of the figure), allowing immediate Recall, or one of three distractor masking conditions (Flash, Invisible, or New Board) is presented for 2000 ms (as shown in the right figure). Finally, in the Recall stage subjects are asked to replicate the pattern shown during the Stimulus stage without making any mistakes.

## Method

### **Figure 2.** Task instructions and board state.

<p float="left">
  <img src="./figs/instructions.png" width="48%" alt="Task instructions">
  <img src="./figs/board.png" width="48%" alt="Task board">
</p>

Subjects were presented with brief instructions on the task before starting, as shown in the left figure above. On the right, a single random board layout of the task is shown. These board layouts randomly change between each trial of the task. Subjects solve 30 trials of each masking condition (Flash, Invisible, New Board) and 30 trials of a no masking condition for a total of 120 trials. Each masking condition is visually depicted in [Figure 1](#figure-1-modified-visual-patterns-test-timeline).

## Results

Our statistical analysis code is stored in [scripts/analysis.Rmd](./scripts/analysis.Rmd) as a R Markdown file. We've knitted an html webpage of the analysis code, which can be viewed in [scripts/analysis.html](./scripts/analysis.html).

### **Figure 3.** Three performance statistic bar charts showing mean pattern size across the four conditions 

<img src="./figs/results_hist_3_by_1.png" alt="Three results histograms" >

> **Note:** The bar chart displays the mean pattern size across the four task conditions. We calculated three performance metrics including the max trial performance, last trial performance, and average trial performance across the last 20 trials. n.s. &ndash; not significant, * &ndash; $p < 0.01$, ** &ndash; $p < 0.001$. 

### **Table 1.** Mean performance and planned contrasts across mask conditions

<table style="border-collapse:collapse;border-spacing:0" class="tg">
<thead>
<tr>
<th></th>
<th colspan="3" style="text-align:center;">Mean (SE)</th>
<th></th>
<th colspan="3" style="text-align:center;">P-value</th>
</tr>
<tr>
<th>Mask Condition</th>
<th>MTP</th>
<th>FTP</th>
<th>ATP</th>
<th>Contrast</th>
<th>MTP</th>
<th>FTP</th>
<th>ATP</th>
</tr>
</thead>
<tbody>
<tr>
<td>None</td>
<td>5.52 (0.17)</td>
<td>3.75 (0.26)</td>
<td>3.94 (0.15)</td>
<td>None vs Flash</td>
<td>0.904</td>
<td>0.088</td>
<td>0.422</td>
</tr>
<tr>
<td>Flash</td>
<td>5.55 (0.24)</td>
<td>4.18 (0.27)</td>
<td>4.08 (0.19)</td>
<td>Invis. vs NB</td>
<td><b>0.003</b></td>
<td>0.314</td>
<td><b>0.002</b></td>
</tr>
<tr>
<td>Invisible</td>
<td>5.25 (0.22)</td>
<td>3.55 (0.23)</td>
<td>3.71 (0.18)</td>
<td>N / F vs I / NB</td>
<td><b>1e-4</b></td>
<td><b>0.003</b></td>
<td><b>1e-4</b></td>
</tr>
<tr>
<td>New Board</td>
<td>4.63 (0.18)</td>
<td>3.30 (0.20)</td>
<td>3.18 (0.18)</td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

> **Note:** MTP, FTP, and ATP refer to maximum, final, and average trial performance, respectively. The two abbreviated contrasts refer to Invisible vs. New Board and None / Flash vs. Invisible / New Board. Significant p-values are presented in bold.

## Data

Subject data is provided in JSON format in the [data/](./data) directory.

### JSON Schema

The JSON schema below is stored in [data/experiment_schema.json](./data/experiment_schema.json).

```json
{
    "$schema": "https://json-schema.org/draft/2020-12/schema",
    "type": "object",
    "title": "Experiment Data",
    "description": "Contains subject information and their trials.",
    "properties": {
        "subjectId": {
            "type": "string",
            "description": "Unique identifier for the subject."
        },
        "trials": {
            "type": "array",
            "description": "List of trials conducted by the subject (size 120).",
            "items": {
                "type": "object",
                "properties": {
                    "trial": {
                        "type": "integer",
                        "description": "Trial index (1-based)."
                    },
                    "maskType": {
                        "type": "string",
                        "enum": ["None", "Flash", "Invisible", "NewBoard"],
                        "description": "Type of visual mask applied in the trial."
                    },
                    "maskMetaData": {
                        "type": "object",
                        "description": "Contains additional metadata for the mask type. When `maskType` is 'NewBoard', it includes 'NewBoardPositions'.",
                        "properties": {
                            "NewBoardPositions": {
                                "type": "array",
                                "description": "Positions of the new board tiles when maskType is 'NewBoard'.",
                                "items": {
                                    "type": "object",
                                    "properties": {
                                        "x": {
                                            "type": "integer",
                                            "description": "X coordinate of the new tile."
                                        },
                                        "y": {
                                            "type": "integer",
                                            "description": "Y coordinate of the new tile."
                                        }
                                    }
                                }
                            }
                        }
                    },
                    "response": {
                        "type": "array",
                        "description": "List of tile keys the subject clicked.",
                        "items": {
                            "type": "string"
                        }
                    },
                    "reactionTime": {
                        "type": "array",
                        "description": "Reaction times recorded in milliseconds.",
                        "items": {
                            "type": "integer",
                            "minimum": 0
                        }
                    },
                    "stimulus": {
                        "type": "array",
                        "description": "List of tile keys presented as stimuli.",
                        "items": {
                            "type": "string"
                        }
                    },
                    "boardPositions": {
                        "type": "array",
                        "description": "All board tile positions, where each tile is defined by its top-left corner coordinates.",
                        "items": {
                            "type": "object",
                            "properties": {
                                "x": {
                                    "type": "integer",
                                    "description": "X coordinate of the tile."
                                },
                                "y": {
                                    "type": "integer",
                                    "description": "Y coordinate of the tile."
                                },
                                "key": {
                                    "type": "string",
                                    "description": "Tile key identifier."
                                }
                            }
                        }
                    }
                },
                "required": ["trial", "maskType", "response", "reactionTime", "stimulus", "boardPositions"]
            }
        }
    },
    "required": ["subjectId", "trials"]
}
```

