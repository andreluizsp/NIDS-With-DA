# Network Intrusion Detection Systems With Domain Adaptation

<div align="justify">

&nbsp;&nbsp;&nbsp;&nbsp;This work advances the traditional model by employing an ensemble of Deep AutoEncoders organized into two stages. In the first stage, each Deep AutoEncoder extracts a distinct set of latent features, with diversity ensured by varying architectural configurations (number of neurons and layers). This structural heterogeneity enables the system to capture multiple perspectives of the data, thereby enhancing its generalization capability. In the second stage, training incorporates both the diversity of the AutoEncoder’s latent spaces and the accuracy of the resulting model. This design allows the model to integrate complementary information learned by each AutoEncoder, thereby optimizing overall performance. Joint training is conducted in a multi-objective setting, where feature extraction and classification are tuned simultaneously. By accounting for latent diversity alongside global accuracy, the model preserves its effectiveness even under varying network conditions.

<p align="center">
  <img src="PropostaQualificacaoArqAE3.png" alt="Texto alternativo" width="400"/>
</p>
   
</div>

# In summary, the main objectives of this work are:

• To evaluate the generalization capability of traditional ML techniques in NIDS, assessing their performance across multiple domains, where experiments demonstrate their limited ability to generalize;

• Develop an ML model based on an ensemble of Deep AutoEncoders, designed to extract diverse features and improve generalization, thereby enabling deployment across heteroge neous network domains for NIDS;

• To compare the results obtained from training with varying architectural configurations of the Deep Autoencoder ensem- ble, using different datasets to pursue DA.


# Project Setup

Start by cloning the project (Install git: https://git-scm.com/download):

Shell: # git clone --depth=1 https://github.com/andreluizsp/NIDS-With-DA.git && cd NIDS-With-DA

This will create a new directory called "NIDS-With-DA" containing the following files:

$ ls

LICENSE  MakeCSV.py Packets README.md Rogue_OCCS_SVM.ipynb dataset.csv
Import Rogue_OCCS_SVM.ipynb in Juniper or Google Colab
  https://colab.research.google.com/drive/1rbxLpr-232kK-4MhV1nt5H3Qaaz-ekb7?usp=sharing
Import dataset.csv to Goole Drive or change the cell below
  df_orig = pd.read_csv('/content/drive/MyDrive/datasets/dataset.csv')
Directory Packages vs. Script MakeCSV.py
  1) Inside the Packages directory are the packages used in this project (357 Access Points - APs)

  2) Script MakeCSV.py must be in the same directory as the .pcaps files to extract the features 
     of all APs with the command below:

     Shell: # MakeCSV.py > dataset.csv
