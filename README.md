Solution to an interesting task from Artificial Intelligence Implementation Show Winter Contest.

The problem is about hunting "ghosts" which intead implies detecting AI fake faces. Task Restriction is that train_data has only true images (real people photos), while test_data has both types of faces mixed. The goal is to build classifier without using any external data. 

My solution finds 201 faces that differ most by Standard deviation of channels of image. Code assumes those are Fake images and trains simple classifier. Achieveng about 0.75 F1-score.
