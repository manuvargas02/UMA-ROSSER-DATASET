# UMA-ROSSER-DATASET

Dataset created for the article "Surgeon gesture recognition sensor system for a laparoscopic suture manoeuvre".

*Author*: Manuel Vargas-Puga

*Contact info*: [manu02@uma.es](mailto:manu02@uma.es)

*Affiliation*: University of Malaga, [Medical Robotics Lab](https://medicalrobotics.uma.es/)

## INTRODUCTION
Laparoscopic surgery, a type of minimally invasive abdominal surgery, offers numerous benefits, including reduced mortality, shorter hospital stays, and lower costs. However, it also presents challenges such as a steep learning curve, loss of 3D vision and ergonomic issues. To address these challenges, robotic systems have been introduced to improve precision and control. This paper proposes a robust kinematic data acquisition system for capturing surgeon movements during laparoscopic procedures using two infrared trackers and a real-time Kalman filter, which reduces positioning errors and estimates tool poses when tracking is lost. Using this system, a dataset was created from the kinematic data of two laparoscopic instruments during a surgical suture manoeuvre. This dataset was used to train a gesture recognition system capable of identifying surgeon actions in the manoeuvre, contributing to the advancement of human-robot collaboration in laparoscopic surgery.

<div align="center">
  <img src="https://github.com/user-attachments/assets/5eb78b7e-8ec4-4243-a47d-59b87b90cfdf" alt="image" width="400" height="300">
</div>

## DATASET FILES
This repository contains all the files that make up the dataset created in the article "Surgeon gesture recognition sensor system for a laparoscopic suture manoeuvre." The dataset consists of the kinematic data provided by two laparoscopic instruments of the movements performed during a Rosser laparoscopic suture, in which 3 turns are made to tie the knot. The captured dataset consists of 9 different users performing the suture manoeuvre 5 times each, on a suture pad inside a pelvi-trainer (an abdominal simulator). Users were named with the letters A to I, so each trial can be identified by the index of the user followed by the index of the trial. For example, the second trial of user B was labelled as B02.

This repository provides the following folders:

- **Videos folder**: Contains the MP4 video files of each trial, used to label the data manually by a single user watching the videos of the manoeuvre and labeling the gestures being performed at each moment using MATLAB's Video Labeler software.

- **Kinematic data folder**: Contains all kinematic data of the surgical instruments during the suture. Table 1 shows the variables captured for each trial.

- **Labels folder**: Contains a text file for each trial with the corresponding label for each kinematic sample.

- **Questionnaire folder**: Contains a text file for each trial with the user's answers to questions about their age, experience in laparoscopic surgery, and other details.

The following table shows the variables captured in the kinematic data file and their corresponding units. These include the components of position, orientation, linear and angular velocities of each tool (left and right), as well as the timestamp. The data is sampled at 30 Hz.

<div align="center">
  
| Index  | Label                                                 | Components | Units  |
|--------|-------------------------------------------------------|------------|--------|
| 1-3    | LTTP_position_<x,y,z>                                 | 3          | m      |
| 4-6    | LTTP_orientation_<x,y,z>                              | 3          | rad    |
| 7-9    | LTTP_velocity_linear_<x,y,z>                          | 3          | m/s    |
| 10-12  | LTTP_velocity_angular_<x,y,z>                         | 3          | rad/s  |
| 13-15  | RTTP_position_<x,y,z>                                 | 3          | m      |
| 16-18  | RTTP_orientation_<x,y,z>                              | 3          | rad    |
| 19-21  | RTTP_velocity_linear_<x,y,z>                          | 3          | m/s    |
| 22-24  | RTTP_velocity_angular_<x,y,z>                         | 3          | rad/s  |
| 25     | timestamp                                             | 1          | ms     |

*Table 1: Variables captured in the kinematic data file.*

</div>

## CITE
You are free to use this dataset for any purpose (research, teaching, commercial applications, etc.), but proper citation of the following reference is required in any resulting work or publication. The citation is provided in BibTeX format:

```bibtex
@misc{gesture_recognition,
   abstract = {Laparoscopic surgery, a type of minimally invasive abdominal surgery, offers numerous benefits, including reduced mortality, shorter hospital stays, and lower costs. However, it also presents challenges such as a steep learning curve, loss of 3D vision and ergonomic issues. To address these challenges, robotic systems have been introduced to improve precision and control. This paper proposes a robust kinematic data acquisition system for capturing surgeon movements during laparoscopic procedures using two infrared trackers and a real-time Kalman filter, which reduces positioning errors and estimates tool poses when tracking is lost. Using this system, a dataset was created from the kinematic data of two laparoscopic instruments during a surgical suture manoeuvre. This dataset was used to train a gesture recognition system capable of identifying surgeon actions in the manoeuvre, contributing to the advancement of human-robot collaboration in laparoscopic surgery.},
   author = {Manuel Vargas-Puga and Juan M Herrera-López and Antonio J Reina-Terol and Víctor F Muñoz},
   keywords = {Gesture Recognition,Human-Robot Collaboration,Index Terms-Laparoscopic Surgery,Kalman Filter,Suture Manoeuvre,Tracking System},
   title = {Surgeon gesture recognition sensor system for a laparoscopic suture manoeuvre},
}
