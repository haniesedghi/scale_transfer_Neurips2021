# scale_transfer_Neurips2021

![](covex_hull_with_size_and_fits.png?raw=true "Title")
A. The performance of downstream (8 different tasks) vs of upstream based on more than 3K different Vision Transformer(ViT) models with different configurations. The models are pre-trained on JFT and evaluated in few-shot settings (25 shots).  We consider the convex hull of the points as well since it captures the performance of a randomized classifier made by choosing these models with different probabilities. As the upstream performance improves, the downstream performance starts to saturate. 
    Even if US accuracy reaches 100% accuracy, the DS accuracy will not reach the 100% accuracy and saturates at a lower value. 
    We observe a non-linear relationship between upstream and downstream accuracy and model the relationship with a power law function to predict the downstream performance given the upstream performance. The plot also show horizontal line which is the predicted downstream accuracy if upstream accuracy reaches 100%. We investigate DS-vs-US plots instead of the usual DS-vs-scale plots to capture the effect of hyper-parameter choices and to account for the fact that the scaling impacts downstream performance through upstream performance. 


![](merged_fitting_error.png?raw=true "Title")
 B. the effect of sample size on power law curves. The curves are fitted to the convex hull of experiments as well as all data points from Figure A. We plot the predictions from the power law curve on the higher US accuracies to the ground truth (prediction target) and calculate fit and prediction accuracy as the number of samples changes. These errors are very small for both choices of data points and robust to the number of samples when the number of samples is as low as 500.
