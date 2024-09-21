# cbd-asd-eeg
Code for Cazares et al. paper looking at aperiodic signal features in EEG from boys with low functioning autism before and after chronic cannabidiol treatment


01_EEG_Preprocessing: 
Loads .eeg files and epochs signals. Applies AutoReject (Global), ICA, AutoReject (Local) procedures. Concatenate processed epochs and apply a hamming window taper.

02_EEG_PSD_FOOOF: 
Loads processed EEG (.fif), computes power spectral density and apply specparam (FOOOF) procedures.

03_EEG_Extract_Features: 
Loads specparam (FOOOF) outputs (.json), calculates periodic and aperiodic signal features.

04_EEG_Behavior_Models: 
Loads calculated behaviora assessments and signal features (.csv) and runs linear mixed models relating 7-COOH-CBD metabolite levels in blood to behavioral assessment outcomes and EEG signal features.

05_EEG_Mediation_Analysis: 
Loads calculated behaviora assessments and signal features (.csv) and runs mediation analyses relating 7-COOH-CBD metabolite levels in blood to behavioral assessment outcomes and EEG signal features.
