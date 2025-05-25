Donut on TextOCR experiments
---
The Donut Models directory contains the Python notebooks used, 1 for each experiment and 1 for core-set generation exclusively:
- donut_on_textocr.ipynb - Baseline experiment with Donut on TextOCR with no modifications
- donut_on_textocr_bboxes.ipynb - Donut experimentation with TextOCR's data as individual bounding boxes rather than whole images + label smoothing
- donut_on_textocr_curriculum.ipynb - Donut experimentation building off previous experiment with curriculum learning
- donut_on_textocr_optuna.ipynb - Donut experimentation building off of the original bounding boxes experiment using Optuna
- coreset-generation.ipynb - The code for generating the three core-sets used for training
- donut_on_coresets.ipynb - Donut experimentation using the core-sets generated in coreset_generation.ipynb, builds off the original bounding boxes experiment

The other files are more miscellaneous and were created mostly for verification of certain qualities.

The Donut Results directory contains the results of each experiment:
 - results_bboxes.json - The CER and model output/ground truth pairs on the test dataset in the TextOCR with bounding boxes experiment
 - results_best_lenpenalty_labelsmooth.json - The best CER and model output/ground truth pairs on the test dataset in the TextOCR with bounding boxes + label smoothing experiment
 - results_bboxes_lenpenalty_labelsmooth_replicate.json - The CER and model output/ground truth pairs on the test dataset in the TextOCR with bounding boxes + label smoothing experiment that can be replicated due to having random seed information
 - results_curriculum.json - The CER and model output/ground truth pairs for the curriculum learning experiment
 - results_diversityjson - The CER and model output/ground truth pairs for the diversity core-set experiment
 - results_hard.json - The CER and model output/ground truth pairs for the hard example core-set experiment
 - results_dh.json - The CER and model output/ground truth pairs for the hybrid diversity and hard strategy

Finally, the coreset_info txt file contains a Drive link to where the core-sets are hosted.
