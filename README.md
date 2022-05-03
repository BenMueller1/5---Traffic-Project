I began by using the parameters that were used in the lecture notes. This model performed very
poorly with a loss of 3.4935 (using cross-entropy loss function) and an accuracy of only 5.39%
( which is only a little over twice as good as guessing randomly). Another thing I noticed
was that it only improved marginally after the first epoch (going from 5.1 to 3.59 loss) 
and the loss only decreased by 0.09 over the next 9 epochs.

Adding another convolution layer followed by another max pooling layer helped immensely, reducing loss to 0.2438 and increasing the accuracy to 93.84%

I tried changing the number of nodes in the hidden layer to 50000 for fun (instead of 128).
This was a stupid idea.

I changed the number of nodes in the hidden layer down to 2056 and changed the dropout to 0.4,
then added another hidden layer with 256 nodes with a dropout of 0.25. 
This had good results, with an accuracy of 94.42% and a loss of 0.2185

I tried increasing the first droupout rate to 0.7 and the second one to 0.5, I also added a dropout after the flattening (rate = 0.7). (TERRIBLE IDEA!) accuracy = 6%

I then tried the same thing but with the dropout after the flattening excluding, which
resulted in another low accuracy, so I set my dropout rates back to what they were previously

Tried decreasing my droupout rates to 0.3 and 0.1
accuracy: 93.6%
loss: 0.2580

Tried removing the second max pooling layer and put the dropout rates back to 0.4 and 0.25
This result was about the same (with a slightly higher loss) to when I had the same setup with the addition of the second max pooling layer, so I added the last max pooling layer back in
