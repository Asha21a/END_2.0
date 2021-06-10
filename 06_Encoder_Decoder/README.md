Task
<ul><li>
encoder: an RNN/LSTM layer takes the words in a sentence one by one and finally converts them into a single vector. </li>
<li> this single vector is then sent to another RNN/LSTM that also takes the last prediction as its second input. </li>
<li> Then we take the final vector from this Cell and send this final vector to a Linear Layer </li>
<li> and make the final prediction. </li> </ul>

This is how it should look:
embedding
word from a sentence +last hidden vector -> encoder -> single vector
single vector + last hidden vector -> decoder -> single vector
single vector -> FC layer -> Prediction
