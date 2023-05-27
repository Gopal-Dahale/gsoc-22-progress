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

## Tuned some hyperparameters

- Cropped to 10 $\times$ 10 instead of 8 $\times$ 8 for the Electron-Photon dataset.
- Used batch size of 1024 over the full dataset.
- Tried data augmentation techniques like
    - Random flip
    - Random rotation

---

## With Data augmentation

<p class='small-font null'> Train AUC: <b>0.70</b>  |  Test AUC: <b>0.70</b></p>

<img src="images/EP3-QCNNHybrid-1-1/withDA/acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-1/withDA/loss.png"  height="auto" width="450px">
<br class='null'>
<img src="images/EP3-QCNNHybrid-1-1/withDA/val_acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-1/withDA/val_loss.png"  height="auto" width="450px">


---

## Without Data augmentation

<p class='small-font null'> Train AUC: <b>0.76</b>  |  Test AUC: <b>0.759</b></p>

<img src="images/EP3-QCNNHybrid-1-1/withoutDA/acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-1/withoutDA/loss.png"  height="auto" width="450px">
<br class='null'>
<img src="images/EP3-QCNNHybrid-1-1/withoutDA/val_acc.png"  height="auto" width="450px">
<img src="images/EP3-QCNNHybrid-1-1/withoutDA/val_loss.png"  height="auto" width="450px">

---

## What now?

- The data augmentation might need tuning. It has parameters like factor of rotation and fill mode.
- Testing these might give some better results.
- Decreasing the cropping might also give some better results.

---

## Status
<div class="container">

<div class="col" >
<span style="color:#97D077"> Done: </span>

- Trained QCNNHybrid on EP with JAX + Pennylane and got some good results than past ones.
- Used data augmentation techniques but they need some fine tuning.
</div>

<div class="col">
<span style="color:#7EA6E0"> Goals for next week: </span>

- Tuning data augmentation and other hyperparams.
- Work on the classical models to improve their AUC.
</div>


</div>

