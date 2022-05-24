# Random notes for nanopore sequencing

## Guppy 6.0.1 optimised settings for RTX3080 (10GB VRAM)
Chunk size was fixed to 3000 as accuracy score plataeus at this size.
Flowcell = FLO-MIN106
Kit = SQK-RPB004
Note: Chunks_per_runner could be increased if demultiplexing and trim barcodes is turned off
#### Guppy HAC basecalling 
```
guppy_basecaller --device "cuda:0" --chunk_size 3000 --chunks_per_runner 768 --gpu_runners_per_device 4 --min_qscore 7 --barcode_kits SQK-RPB004 --trim_barcodes --num_barcoding_buffers 16 --flowcell FLO-MIN106 --kit SQK-RPB004 --compress_fastq --input_path Patient_21_19-05-2022/ --save_path guppy_basecalls --recursive
```
Samples/s = 1.3299e+07

#### Guppy SUP basecalling
Chunk size was fixed to 3000 as accuracy score plataeus at this size. 
```
guppy_basecaller --device "cuda:0" --chunk_size 3000 --chunks_per_runner 200 --gpu_runners_per_device 4 --min_qscore 7 --barcode_kits SQK-RPB004 --trim_barcodes --num_barcoding_buffers 16 --config dna_r9.4.1_450bps_sup.cfg --compress_fastq --input_path . --save_path guppy_basecalls --recursive
```
Samples/s = 3.73233e+06
