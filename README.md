# tensorflowModel

"rats" folder stores SSD model architecture trained on roughly 700 images of rats.


ratDetection2.py handles the detection of rats in a video feed or folder of images.

Loads frozen inference graph and analyzing necessary tensors (classes (name), num_detections (number of rats detected), detection_scores (confidence %), detection_boxes (box coordinates of detected rats, sorted in order of highest confidence to lowest)

From here the boxes are drawn and data is analyzed ensuring that the confidence exceeds a particular threshold (70%), boxes and score listed are resorted to better organize and access data
From here each image is analyzed and labeled images with high confidence ratings are sorted into one directory while ones with subpar confidence ratings are sorted into another.
For each image in the high confidence directory a CSV is created detailing it's head and tail positions.
