Solution to an interesting task from Artificial Intelligence Implementation Show Winter Contest. 

The problem is about hunting "ghosts" which intead implies detecting AI fake faces. Task Restriction is that train_data has only true images (real people photos), while test_data has both types of faces mixed. The goal is to build classifier without using any external data. 

My first solution finds 201 faces that differ from Train Real Images most by Standard deviation of channels of image. Code assumes those are Fake images and trains simple classifier. Achieveng about 0.75 F1-score.

By analyzing data, i found that fake faces have smooth but combined faces. Using this observation i create fake data by merging two random images. Then i use resnet18 embeddings and on this data i train simple sklearn Logistic Regression. This solution achives 0.92 F1-score.

Repository contains data folder with train and test folders and solution written in Python language in Jupyter notebook format.

Problem can be found here: https://judge.nitro-ai.org/competitions/aiis/aiis-winter-contest/2

Special thanks to Morariu Tudor @morariutudor and Alexandru Ionut Tone @tonealexandru236 for designing this problem.
