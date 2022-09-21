---
revealOptions:
  transition: 'fade'
  transitionSpeed: 'fast'
  width: 1400
---
<style>
.container{
    display: flex;
}
.col{
    flex: 1;
}
.small-font{
    font-size:20px;
}

.null{
    padding:0px;
    margin:0px;
}

</style>

#### Tuned some hyperparameters

- Cropped to 10 $\times$ 10 instead of 8 $\times$ 8 for the Electron-Photon dataset.
- Used batch size of 1024 over the full dataset.
- Tried data augmentation techniques like
    - Random flip
    - Random rotation

---

###### With Data augmentation

<p class='small-font null'> 1 qubit | 1 layer | Train AUC: <b>0.70</b>  |  Test AUC: <b>0.70</b></p>

<img src="images/EP3-QCNNHybrid-1-1/withDA/acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-1/withDA/loss.png"  height="auto" width="450px">
<br class='null'>
<img src="images/EP3-QCNNHybrid-1-1/withDA/val_acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-1/withDA/val_loss.png"  height="auto" width="450px">


---

###### Without Data augmentation

<p class='small-font null'> 1 qubit | 1 layer | Train AUC: <b>0.76</b>  |  Test AUC: <b>0.759</b></p>

<img src="images/EP3-QCNNHybrid-1-1/withoutDA/acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-1/withoutDA/loss.png"  height="auto" width="450px">
<br class='null'>
<img src="images/EP3-QCNNHybrid-1-1/withoutDA/val_acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-1/withoutDA/val_loss.png"  height="auto" width="450px">

---

###### More layers

<p class='small-font null'> 1 qubit | 2 layers | Train AUC: <b>0.77</b>  |  Test AUC: <b>0.7684</b></p>

<img src="images/EP3-QCNNHybrid-1-2/acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-2/loss.png"  height="auto" width="450px">
<br class='null'>
<img src="images/EP3-QCNNHybrid-1-2/val_acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-2/val_loss.png"  height="auto" width="450px">

---

- Increasing the number of qubits from 1 to 2 gives similar results.
- Try Cropping to 12 $\times$ 12 instead of 10 $\times$ 10.

---
###### With Data augmentation

<p class='small-font null'> 1 qubit | 1 layer | Train AUC: <b>0.68</b>  |  Test AUC: <b>0.68</b></p>

<img src="images/EP3-QCNNHybrid-1-1/withDA/12.12/acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-1/withDA/12.12/loss.png"  height="auto" width="450px">
<br class='null'>
<img src="images/EP3-QCNNHybrid-1-1/withDA/12.12/val_acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-1/withDA/12.12/val_loss.png"  height="auto" width="450px">


---

###### Without Data augmentation

<p class='small-font null'> 1 qubit | 1 layer | Train AUC: <b>0.767</b>  |  Test AUC: <b>0.767</b></p>

<img src="images/EP3-QCNNHybrid-1-1/withoutDA/12.12/acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-1/withoutDA/12.12/loss.png"  height="auto" width="450px">
<br class='null'>
<img src="images/EP3-QCNNHybrid-1-1/withoutDA/12.12/val_acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-1/withoutDA/12.12/val_loss.png"  height="auto" width="450px">

---

###### Result with full Quark Gluon (40 x 40)


<p class='small-font null'> 1 qubit | 1 layer | Train AUC: <b>0.723</b>  |  Test AUC: <b>0.699</b></p>

<img src="images/QG3-QCNNHybrid-JAX-1-1/acc.png"  height="auto" width="450px">
<img src="images/QG3-QCNNHybrid-JAX-1-1/loss.png"  height="auto" width="450px">
<br class='null'>
<img src="images/QG3-QCNNHybrid-JAX-1-1/val_acc.png"  height="auto" width="450px">
<img src="images/QG3-QCNNHybrid-JAX-1-1/val_loss.png"  height="auto" width="450px">


---

## Status
<div class="container">

<div class="col" >
<span style="color:#97D077"> Done: </span>

- Trained QCNNHybrid on EP with JAX + Pennylane and got some good results than past ones.
- Trained on QG but not very good results.
- Used data augmentation techniques but seems not promising for QCNN.
</div>

<div class="col">
<span style="color:#7EA6E0"> Goals for next week: </span>

- Documentation and cleaning up stuff.
- Setting github repo properly.
</div>


</div>

