# ChestX-ray Deseases Detection

The assignment was completed on the Kaggle platform. To install dependencies:

```
pip3 install -r requirements.txt
```
1) Used the out-of-the-box Faster R-CNN with MobileNetV3 backbone from torchvision. Ideally, a more sophisticated loss function such as Focal Loss should be employed to mitigate class imbalance issues.
2) The available dataset is critically small; a meaningful solution would require significantly more data.
3) It would be better to restructure the dataset into the standard COCO format to make hypothesis testing and model evaluation more robust.
4) Evaluation metrics should preferably be logged using tools like wandb or similar platforms.
5) The code for computing mAP was partially adapted from GitHub to fit the current data format. Notably, there is no true test set—evaluation is performed on the validation set. The inference pipeline produces a prediction dataFrame (`df_pred`), which is then compared against the ground-truth annotations; mAP is computed solely based on the class labels and bounding boxes from these two dataframes.
