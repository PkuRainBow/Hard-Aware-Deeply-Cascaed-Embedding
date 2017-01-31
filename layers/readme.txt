Please add the pair_fast_loss_layer

Edit the caffe.prototxt to add the layer parameters like this :


message PairFastLossParameter {
  //margin for dissimilar pair
  optional float margin = 1 [default = 1.0];
  optional float hard_ratio = 2 [default = 1.0];
  optional float use_pos = 3 [default = 0];
}

use_pos : means only consider the negative pairs or consider all the positive pairs and negative pairs
