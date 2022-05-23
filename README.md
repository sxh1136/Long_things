# Long_things
## Optimised guppy HAC basecalling for mcschaik workstation
```
guppy_basecaller --flowcell FLO-MIN106 --kit SQK-RPB004 --recursive -x auto --input_path ~/Documents/Stan/VLP_impact/Patient_21_19-05-2022/ --save_path ~/Documents/Stan/VLP_impact/Patient_21_19-05-2022/guppy_basecalls --chunk_size 3000 --chunks_per_runner 290 --gpu_runners_per_device 4 --compress_fastq
```
Chunk size was fixed to 3000 as accuracy score plataeus at this size. Chunks_per_runner and --gpu_runners_per_device were optimised for sample/s
samples/s: 1.08963e+07

Did try Super accuracy mode but it was very slow even with a RTX3080
