# DepressionDetect
Detecting depression using DAIC WOZ dataset

This project is inspired by the brilliant research work of Tuka Alhanai, Mohammad Ghassemi, and James Glass of MIT on "Detecting Depression with Audio/Text Sequence Modeling of Interviews".

Link to their paper: http://groups.csail.mit.edu/sls/publications/2018/Alhanai_Interspeech-2018.pdf

The aim of this project is to completely implement the model proposed in the research paper, and look for possible modifications that would optimize the model further.
The following modifications have been made to the architecture of the proposed model in the paper:
  - Initially, we have implemented Bidirectional LSTMs on only textual data of the DIAC-WOZ database, due to the lack of efficient hardware to process the audio data.
  - Instead of using 2 layers of BiLSTMs, we have introduced 3 layers.
  - Processing of the input textual data has been considered using the original Doc2Vec segment level analysis approach.
  - We have also used an embedding layer instead of the Doc2Vec function.
  - Due to the absence of the audio processing mode, our architecture is currently simple and not multimodal as proposed in the research paper.
  - We have experimented with several changes in the hyperparameters used in the model- the learning rate (0.01 - 0.1), the optimizer technique (SGD, Adam), number of epochs (50-300), the type of loss (binary vs. categorical cross entropy), the activation function for the Dense layer (sigmoid vs. softmax vs. ReLU) and so on.

The result has been that the model's accuracy stabilized at 72.9%, with the loss (mse) being 0.590, for 300 epochs. 
The model was using categorical cross entropy, with activation as Softmax.


Authors - Amit, Prahlad and Savitru 
