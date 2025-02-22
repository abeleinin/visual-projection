# Visual Projection Experiment Data

This repository is a WIP on open sourcing a dataset gathered from cognitive science research on visual projection. In the near future, this repository will include data from 40 participants solving this [modified visual paterns test](https://projection-experiment.vercel.app/).

## Table of Contents

- [Method](#method)
- [Results](#results)
- [Data](#data)
- [Citation](#citation)

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

### **Figure 3.** Three performance statistic bar charts showing mean pattern size across the four conditions 

<img src="./figs/results_histogram_3_by_1.jpg" alt="Three results histograms" >

> **Note:** The bar chart displays the mean pattern size across the four task conditions. We calculated three performance metrics including the max trial performance, last trial performance, and average trial performance across the last 20 trials. n.s. - not significant, * p-value < 0.05, ** p-value < 0.005, *** p-value < 0.0005. 

### **Table 1.** Mean performance and planned contrasts across mask conditions

<table style="border-collapse:collapse;border-spacing:0" class="tg"><thead><tr><th style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal"></th><th style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal" colspan="3">Mean (SE)</th><th style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal"></th><th style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal" colspan="3">P-value</th></tr></thead>
<tbody>
<tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Mask Condition</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">MTP</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">FTP</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">ATP</td>
<td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Contrast</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">MTP</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">FTP</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">ATP</td></tr>
<tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">None</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">5.15 (0.2)</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">3.75 (0.26)</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">3.9 (0.18)</td>
<td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">None vs Flash</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">0.735</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">0.088</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">0.3351</td></tr>
<tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Flash</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">5.23 (0.24)</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">4.18 (0.27)</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">4.09 (0.23)</td>
<td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Invis. vs NB</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">0.019</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">0.314</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal"><span style="font-weight:bold">0.015</span></td></tr>
<tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Invisible</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">4.88 (0.22)</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">3.55 (0.23)</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">3.72 (0.21)</td>
<td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">N / F vs I / NB</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">4e-4</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">0.003</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">4e-4</td></tr>
<tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">New Board</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">4.35 (0.21)</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">3.30 (0.20)</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">3.23 (0.19)</td>
<td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal"></td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal"></td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal"></td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal"></td></tr>
</tbody></table>

> **Note:** MTP, FTP, and ATP refer to maximum, final, and average trial performance, respectively. The two abbreviated contrasts refer to Invisible vs. New Board and None / Flash vs. Invisible / New Board. Significant p-values are presented in bold.

## Data

Data stored in the [data/](./data) directory.

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
            "description": "List of trials conducted by the subject (typically 120).",
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

## Citation

Publication in-review.
