<h2><b>Task</b></h2>
<ol>
<li> encoder: an RNN/LSTM layer takes the words in a sentence one by one and finally converts them into a single vector. </li>
<li> this single vector is then sent to another RNN/LSTM that also takes the last prediction as its second input. </li>
<li> Then we take the final vector from this Cell and send this final vector to a Linear Layer </li>
<li> and make the final prediction. </li> </ol>

<h3><b>This is how it should look:</b></h3>
<ol>
  <li>embedding</li>
  <li>word from a sentence +last hidden vector -> encoder -> single vector</li>
  <li>single vector + last hidden vector -> decoder -> single vector</li>
  <li>single vector -> FC layer -> Prediction</li>

  <h2><b>Solution</b></h2>
  
  <b> Need some more time to complete, please!</b>
