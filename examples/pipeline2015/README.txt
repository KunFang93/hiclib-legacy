NOTE: this pipeline will work with 2015 version of the library. 

This is a current version of the pipeline which we use for processing many Hi-C datasets. This version is for .sra files or fastq.gz files split by two sides. 

Usage: 

1. place .sra files in the fastq folder 
2. edit 00_mapData.py. Specify genome and paths to bowtie, and other arguments
3. provide runs.tsv file as described in 01_makeDatasetsFile.py
4. possibly edit 02_mergeDatasets.py to specify resolutions (especially when working with smaller genomes) 
5. run 02_mergeDatasets.py   -  it will do several things.
    -- merge (if necessary) different .hdf5 files corresponding to one replica of one datasets  
    -- do fragment-level filtering of merged files 
    -- save heatmaps at different resolutions
    -- merge files from different replicas of the same experiment
    -- save heatmaps 

