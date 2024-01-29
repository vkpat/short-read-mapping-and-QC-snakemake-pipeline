This sample test dataset was created by using samtools bam2fq tool to convert bam to fastqs

## Used the GIAB publicly available element data 

- https://ftp-trace.ncbi.nlm.nih.gov/giab/ftp/data/AshkenazimTrio/HG002_NA24385_son/Element_AVITI_20231018/HG002_GRCh38-GIABv3_Element-LngInsert_2X150_55x_20231018.bam

- https://ftp-trace.ncbi.nlm.nih.gov/giab/ftp/data/AshkenazimTrio/HG002_NA24385_son/Element_AVITI_20231018/HG002_GRCh38-GIABv3_Element-LngInsert_2X150_55x_20231018.bam.bai

  ## Bed file
chr4_1Mbp_segments_notinanysegdups.bed:  segments of GRCh38 that don't contain any segdups
Note: First line from bed file was used for filtering the bam file with specific genomic intervals from bed 

## Command used for creating a pair-end fastq files
samtools view -b -L chr4_1Mbp_segments_GRCh38_notinanysegdups.bed HG002_GRCh38-GIABv3_Element-LngInsert_2X150_55x_20231018.bam > HG002_GRCh38-GIABv3_Element-LngInsert_filtered.bam

## Coverting the filtered bam file to fastq files
samtools bam2fq HG002_GRCh38-GIABv3_Element-LngInsert_filtered.bam -1 HG002_GRCh38-GIABv3_Element-LngInsert_1.fq -2 HG002_GRCh38-GIABv3_Element-LngInsert_2.fq

Notes: The fastq files were renamed to the sample1_R1.fastq.gz and sample1_R2.fastq.gz
