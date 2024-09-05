# Summary
This is the raw, un-preprocessed neuroimaging dataset, in BIDS format, for the paper "Valenced tactile information is evoked by 
neutral visual cues following emotional learning". 2024. Imaging Neuroscience.
Please cite this paper if you use this dataset.

# Abstract
Learning which stimuli in our environment co-occur with painful or pleasurable events is critical for survival. 
Previous research has established the basic neural and behavioural mechanisms of aversive and appetitive conditioning; 
however, it is unclear precisely what information content is learned. Here we examined the degree to which aspects of 
the unconditioned stimulus (US) – sensory information vs. affective salience - are transferred to the conditioned 
stimulus (CS). To decode the content of brain activation patterns elicited during appetitive (soft touch) and aversive 
(painful touch) conditioning to faces, a novel approach to using modeling with representational similarity analysis (RSA) 
based on theoretically driven representational patterns of interest (POIs) was applied to fMRI data. Once associations 
were learned through conditioning, globally, the CS reactivated US representational patterns showing conditioning-dependent 
reactivation in specific high order brain regions: In the dorsal anterior cingulate cortex the CS reactivated patterns 
associated with the affective salience of the US – suggesting that, with affective conditioning, these regions carry 
forward the affective associations of the experience.

# Task names:
1: _pain_: Trials in which an aversive pressure stimulus was delivered.  
2: _brush_: Trials in which an appetitive brush stimulus was delivered.  
3: _NA_: Trials in which face stimuli were presented without stimuli to check extinction.  

The following trial types were not used in the analysis for the above paper:  
4: _morph_: Trials in which a series of morphing face stimuli were presented.  
5: _funcloc_: Trials in which a faces vs. houses functional localizer for the fusiform face area (FFA) was presented.  
6: _rest_: Resting-state scans.  
7: _error_: Runs that did not complete correctly - these runs do not have corresponding stimulus timing data.    

# Additional usage notes:
As indicated in our paper, several participants' behavioural data was not available for all trial types due to stimulus delivery errors.
Data was collected using the following procedure:
```
Scanning was conducted on a 3 Tesla GE Discovery magnetic resonance scanner using a 32-channel head coil at Cornell University. 
For each subject, a T1-weighted MPRAGE sequence was used to obtain high-resolution anatomical images 
(repetition time (TR) = 7 ms, echo time (TE) = 3.42 ms, field of view (FOV) 256 x 256 mm slice thickness 1 mm, 176 slices). 
The functional tasks were acquired with the following multi-echo (ME) EPI sequence: TR = 2000 ms, TE1 = 11.7 ms, 
TE2 = 24.2 ms and TE3 = 37.1 ms, flip angle 77°; FOV 240 x 240 mm. A total of 102 slices was acquired with a voxel size of 
3 x 3 x 3 mm.
```

- Anatomical images were not available for `sub-069`, `sub-079`, `sub-094`, `sub-098`, `sub-335`, `sub-359`, and `sub-394` because of errors during acquisition.
- All anatomical images have been anonymized using `pydeface`, except for `sub-065` which was defaced using `fsl_deface` due to pydeface errors.  
- `fslreorient2std` has been applied to all anatomical images to facilitate defacing.  
