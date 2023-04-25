# Protein Crystallization Propensity Prediction Using Deep Learning Approach

<!-- # Installations Needed -->

### Requirements (if using Anaconda)

1. Download Anaconda (64 bit) installer python3.x for linux : https://www.anaconda.com/distribution/#download-section
2. Run the installer : `bash Anaconda3-2019.03-Linux-x86_64.sh` and follow the instructions to install.
3. Install tensorflow-gpu: `conda install tensorflow-gpu`
4. Install imblearn: `conda install -c glemaitre imbalanced-learn`
5. Install sklearn: `conda install -c conda-forge scikit-learn`
<!-- 
# Run the model in Train Mode
  `!CUDA_VISIBLE_DEVICES=? python Train.py` -->
  
<!-- Download the model from here: https://bit.ly/3AvynXa <br/>
Add the downloaded model in model directory. -->

### Requirements (if using Google Colaboratory)

1. Clone this repository in Google Colab : `!git clone https://github.com/onkarsabnis/ProteinCrysPred_DL.git`
2. Go to approapriate directory using cd command
3. Now train the model on the data present in the data directory(it's not the complete data but a subset) by: `!CUDA_VISIBLE_DEVICES=? python Train.py`
4. To run the model on a sample test file do: `!CUDA_VISIBLE_DEVICES=? python Test.py`

### To Train the entire Model

1. Protein sequences have to be saved in a fasta format similar to following format:

.>Seq1 <br />
MPKFYCDYCDTYLTHDSPSVRKTHCSGRKHKENVKDYYQKWMEEQAQSLIDKTTAAFQQG <br />
where '>Seq1' represents the fasta id and the second line is the protein sequence.

2. Download the model files ( all files *.hdf5 and files *.json) by running the following command: <br />
`!wget https://storage.entrydns.org/nextcloud/index.php/s/3ErNEaZiKp39x4N/download`

3. Run the following two commands after downloading the model files: <br />
!unzip download <br />
!rm download <br />

4. To train the model on your own data, run the following command (Train.py and the fasta file have to be in the same directory):<br />
$ !python Train.py <file.fasta>. <br />
Add the trained model in the 'model' directory.

Now to run the model on test file: `!CUDA_VISIBLE_DEVICES=? python Test.py` <br/>
You can change the input file in the code.

