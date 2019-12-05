#  Character Region Awareness for Text Detection  

## Idea

detect text area by exploring each character and affinity between characters.

## Architecture

![]( https://github.com/ChrisWang10/paper/raw/master/img/craft.png )



it's similar to u-net.  The final output has two channels as score maps: the region score and the affinity score.  

## Training

For each training image, it generates ground truth label for the ***region score*** and ***affinity score*** with character level bounding boxes. **region score** represents possibility that given pixel is the center of the character and **affinity score** represents possibility that given pixel is the center of between two characters.



**Ground Truth Generation**

![](https://github.com/ChrisWang10/paper/raw/master/img/craft_gt.png)

**weakly supervised learning**

  real images in a dataset usually have word-level annotations rather character-level annotations. So we can first use easily gettable synthetic images to train a interim model to predict the character region of the real images to get character annotations. 
