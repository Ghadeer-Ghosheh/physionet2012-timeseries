# physionet2012-timeseries

Table of contents
=================

<!--ts-->
   * [About the repository](#About-the-repository)
      * [Background](#Background)
      * [Code](#Code)
   * [Citation](#Citation)
   
<!--te-->

About the repository
============
This repository includes preprcorsessing pipeline for the PhysioNet/Computing in Cardiology Challenge 2012 dataset, creating ready-to-use files for time-series machine learning tasks. 

We also extract the auxiliary static features and outcomes for each of the three sets provided by PhysioNet. An overview of the output files, for each set, is shown in the figure below. 

![alt text](https://github.com/Ghadeer-Ghosheh/physionet2012-timeseries/blob/master/outputs.png)

## Background
The PhysioNet/Computing in Cardiology Challenge 2012 dataset includes six static variable, 35 time-series physiological variables (vital signs, and lab tests etc.) and one time-series variable incidating the adminstration of "mechanical ventilation" over the 48 hour recording.

The data includes 12,000 patient-records equally divided into three sets, sets a,b, and c, respectivly.

The outcomes included in the dataset are: SAPS-I score, SOFA score, Length of stay (days), Survival (days) and In-hospital death (0: survivor, or 1: died in-hospital). 


## Code 


* Please download and unzip ```set-a, set-b, and set-c``` folders in the same directory as this repository. 

* Please also download their corrosponding outcome files ```Outcomes-a.txt, Outcomes-b.tx, and Outcomes-c.txt``` from the physioNet website.  

* First run the ```get_static_df.ipynb``` notebook to extract the static data and outcomes dataframes for the three sets.

* Then run the  ```get_time_series.ipynb``` notebook to extract the physiological time-series data and interventions data tensors. 


## Citation

For the PhysioNet dataset, please cite:
```
@inproceedings{silva2012predicting,
  title={Predicting in-hospital mortality of icu patients: The physionet/computing in cardiology challenge 2012},
  author={Silva, Ikaro and Moody, George and Scott, Daniel J and Celi, Leo A and Mark, Roger G},
  booktitle={2012 Computing in Cardiology},
  pages={245--248},
  year={2012},
  organization={IEEE}
}
```


If you found this code useful, please cite: 
```
@article{ghosheh2024ignite,
  title={IGNITE: Individualized GeNeration of Imputations in Time-series Electronic health records},
  author={Ghosheh, Ghadeer O and Li, Jin and Zhu, Tingting},
  journal={arXiv preprint arXiv:2401.04402},
  year={2024}
}
```

