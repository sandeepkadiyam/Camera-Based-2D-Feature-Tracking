## STRUCTURE OF THE PROJECT

### MP.1 Data Buffer Optimization
I implemented a ring buffer in the project. This ring buffer pushes new elements into the buffer using the .push_back method. Once the buffer is filled with elements, the first element is erased using the .erase method to accept a new element.

### MP.2 Keypoint Detection
I implemented a function that accepts the name of the detector type as an argument. This function uses the if loop to compare the detector type and then creates the respective detector instance. The detect method of this instance performs the keypoint detection except for the Harris detector. I used the Harris implementation from the previous tasks.

### MP.3 Keypoint Removal
I iterated through all the detected keypoints and assigned the keypoints that belong to the defined rectangle region that covers the preceeding vehicle to a vector. I assigned the keypoints vector to the new vector. To check the condition, I used the .contains method of the opencv rectangle datatype.

### MP.4 Keypoint Descriptors
I implemented a function that accepts the name of the descriptor type as an argument. This function uses the if loop to compare the descriptor type and then creates the respective descriptor instance. The compute method of this instance extracts the descriptor information of the keypoints.

### MP.5 Descriptor Matching
I implemented a function that accepts the name of the matcher type adn the name of the selector type as arguments. This function uses two seperate if loops to compare the matcher type and the selector type and then creates the respective instances.

### MP.6 Descriptor Distance Ratio
I set the selectorType variable to SEL_KNN to achieve this task.

### MP.7 Performance Evaluation 1
The number of keypoints on the preceding vehicle for all the 10 images is noted using all the detectors. The spreadsheet can be found [here](https://docs.google.com/spreadsheets/d/15qEtsSWv-XniI4dRZ2-61Og1NYlPFjXcrW8nvQn6bCE/edit?usp=sharing).

### MP.8 Performance Evaluation 2
The number of matched keypoints for all the 10 images is noted using all possible combinations of detectors and descriptors. The spreadsheet can be found [here](https://docs.google.com/spreadsheets/d/1KYlkYlA_ZU0UDF6EnyGotkld0H7ZZLEd35ISgXYXDEY/edit?usp=sharing). The brute force matcher cannot be used for SIFT and SURF as they return a detector type of CV32F. So, the FLANN matcher is used to evaluate the performance of SIFT descriptor.

Note: The AKAZE descriptor works only with the AKAZE keypoints.

### MP.9 Performance Evaluation 3
The time taken for the keypoint detection and the keypoint description for all possible combinations of detectors and descriptors are noted. The spreadsheet can be found [here](https://docs.google.com/spreadsheets/d/18-SBzx40RkORlJZxLgujBo-0tTDJEQNIy9swjK9hjMA/edit?usp=sharing). The brute force matcher cannot be used for SIFT and SURF as they return a detector type of CV32F. So, the FLANN matcher is used to evaluate the performance of SIFT descriptor.

Note: The AKAZE descriptor works only with the AKAZE keypoints.
