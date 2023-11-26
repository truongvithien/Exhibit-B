# Exhibit B

In this phase, we will be focusing on the rendering of the video(s) based on the mocap source and music source.

## Input, Output

**Input**:

For example that we need to render video(s) for 2 models (which the first one is the main model, the second one is the secondary model) based on the mocap source and music source. 

The single input will be a json file that contains the following information:
<!-- table -->
| Input | Type | Example |
| --- | --- | --- |
| `{` |  |  |
| &emsp;`orderId` | **String** | "ABCDEF123456" |
| &emsp;`primaryMocapSrc` | **String** | "path-to-mocap-(moveai-output)-source.fbx"  |
| &emsp;`primaryModelCode` | **String** | "Betakkuma" |
| &emsp;`secondaryModelCodes` | **String** (separated by comma) | "Latte" |
| &emsp;`musicSrc` | **String** | "path-to-music-source.mp3" |  
| &emsp;`musicStartTime` | **Number** | 0 |
| &emsp;`musicEndTime` | **Number** | 10000 | 
| `}` |  |  |


**Output**: 

The output will be video files (mp4) that contains the rendered video of the primary model and the secondary model(s) based on the mocap source and music source.

The naming convention of the output video files will be `{orderId}-{modelCode}.mp4` where `orderId` is the `orderId` from the input and `modelCode` is the `primaryModelCode` or `secondaryModelCode` from the input.

Example: `ABCDEF123456-Betakkuma.mp4` and `ABCDEF123456-Latte.mp4`


### Changelog


