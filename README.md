# Random notes for nanopore sequencing
## Guppy HAC basecalling for RTX3080
Chunk size was fixed to 3000 as accuracy score plataeus at this size. 
```
guppy_basecaller --device "cuda:0" --chunk_size 3000 --chunks_per_runner 768 --gpu_runners_per_device 4 --min_qscore 7 --barcode_kits SQK-RPB004 --trim_barcodes --num_barcoding_buffers 16 --flowcell FLO-MIN106 --kit SQK-RPB004 --compress_fastq --input_path Patient_21_19-05-2022/ --save_path guppy_basecalls --recursive

```

## Guppy SUP basecalling for RTX3080
Chunk size was fixed to 3000 as accuracy score plataeus at this size. 
```
guppy_basecaller --device "cuda:0" --chunk_size 3000 --chunks_per_runner 200 --gpu_runners_per_device 4 --min_qscore 7 --barcode_kits SQK-RPB004 --trim_barcodes --num_barcoding_buffers 16 --config dna_r9.4.1_450bps_sup.cfg --compress_fastq --input_path . --save_path guppy_basecalls --recursive
```
3.73233e+06
