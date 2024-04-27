# TrackEval
Eval varios tracking metrics

run_mot_challenge.py

Run example:
run_mot_challenge.py --USE_PARALLEL False --METRICS Hota --TRACKERS_TO_EVAL Lif_T

Command Line Arguments: Defaults, # Comments
    Eval arguments:
    
        'USE_PARALLEL': False,
        
        'NUM_PARALLEL_CORES': 8,
        'BREAK_ON_ERROR': True,
        'PRINT_RESULTS': True,
        'PRINT_ONLY_COMBINED': False,
        'PRINT_CONFIG': True,
        'TIME_PROGRESS': True,
        'OUTPUT_SUMMARY': True,
        'OUTPUT_DETAILED': True,
        'PLOT_CURVES': True,
    Dataset arguments:
        'GT_FOLDER': os.path.join(code_path, 'data/gt/mot_challenge/'),  # Location of GT data
        'TRACKERS_FOLDER': os.path.join(code_path, 'data/trackers/mot_challenge/'),  # Trackers location
        'OUTPUT_FOLDER': None,  # Where to save eval results (if None, same as TRACKERS_FOLDER)
        'TRACKERS_TO_EVAL': None,  # Filenames of trackers to eval (if None, all in folder)
        'CLASSES_TO_EVAL': ['pedestrian'],  # Valid: ['pedestrian']
        'BENCHMARK': 'MOT17',  # Valid: 'MOT17', 'MOT16', 'MOT20', 'MOT15'
        'SPLIT_TO_EVAL': 'train',  # Valid: 'train', 'test', 'all'
        'INPUT_AS_ZIP': False,  # Whether tracker input files are zipped
        'PRINT_CONFIG': True,  # Whether to print current config
        'DO_PREPROC': True,  # Whether to perform preprocessing (never done for 2D_MOT_2015)
        'TRACKER_SUB_FOLDER': 'data',  # Tracker files are in TRACKER_FOLDER/tracker_name/TRACKER_SUB_FOLDER
        'OUTPUT_SUB_FOLDER': '',  # Output files are saved in OUTPUT_FOLDER/tracker_name/OUTPUT_SUB_FOLDER
    Metric arguments:
        'METRICS': ['HOTA', 'CLEAR', 'Identity', 'IDEucl']
"""


Structurs directories : 

Load files : /data
Load gt.txt : /data/gt/mot_challenge/HT-train/1/gt/gt.txt
Load seqinfo : /data/gt/mot_challenge/HT-train/1/seqinfo.ini
Detect results : /data/trackers/mot_challenge/HT-train/1/data/1.txt
HT-Train txt : /data/gt/mot_challenge/seqmaps/HT-train.txt


Do not forget that the settings for the number of images, as well as their information, depend on the seqinfo.ini file. Customize this file for yourself before running the test!!!!


The results of the graphics test after the tests can be found in the directory: data/trackers/mot_challenge/HT-train


For Example : 

![pedestrian_plot](https://github.com/Ruslan-1502/TrackEval/assets/82501852/c51c5148-541a-4bb8-96ea-2b8c6aa6921a)




