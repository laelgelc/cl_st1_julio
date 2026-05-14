# Corpus Linguistics - Study 1 - Julio

## Phase 1 - Tagging with Biber Tagger

- Tag the CEP corpus;
- Prepare Biber's dimension scores output data in Excel format.

## Phase 2 - Tagging with Biber Tagger considering individualised prompt texts

The goal of Phase 2 is to prepare the CEP corpus for analysis with the Biber Tagger and to extract Biber's (1988) linguistic feature data and Dimension Scores from the tag count output.

This phase includes the following steps:

1. **Prepare the corpus for tagging**
   - Read the original `.txt` files from `cl_st1_ph2_julio/corpus/01_CEP`;
   - Copy the files to `cl_st1_ph2_julio/corpus/02_CEP_fixed`;
   - Replace curly inverted commas with straight quotes:
     - `“` and `”` are replaced with `"`;
     - `‘` and `’` are replaced with `'`.

2. **Format the corpus files**
   - Read the fixed files from `cl_st1_ph2_julio/corpus/02_CEP_fixed`;
   - Write the processed files to `cl_st1_ph2_julio/corpus/03_CEP_fixed`;
   - Insert a space between digits and letters, for example `1a` becomes `1 a`;
   - Wrap each text line into groups of up to 10 words, while preserving blank lines.

3. **Tag the prepared corpus**
   - Use the Biber Tagger on the processed corpus files;
   - Store the tagged output in `cl_st1_ph2_julio/corpus/04_CEP_tagged`.

4. **Extract Biber's linguistic feature data**
   - Use the `sas_to_excel.sh` shell script in `cl_st1_ph2_julio/corpus/05_CEP_sas_to_excel`;
   - Convert the Biber Tag Count output into a tabular format importable into Excel;
   - Extract:
     - Normed Frequency Counts for the linguistic features;
     - Biber's Dimension Scores.

The main Phase 2 notebook is:

- `cl_st1_ph2_julio/cl_st1_ph2_julio.ipynb`

The main Phase 2 outputs are:

- `cl_st1_ph2_julio/corpus/05_CEP_sas_to_excel/counts.txt.excel.tab`
- `cl_st1_ph2_julio/corpus/05_CEP_sas_to_excel/counts.txt.excel.tab.xlsx`