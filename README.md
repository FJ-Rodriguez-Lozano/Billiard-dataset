# Billiard-dataset
Billiard-dataset is a collection of recordings made for the scientific paper titled: "*3D reconstruction system and multi-object local tracking algorithm designed for billiards*". The main objective is the creation of a system to perform a reconstruction of billiards moves in a 3D virtual world and a new multi-object tracking algorithm applied to billiards. 

![alt text](https://github.com/FJ-Rodriguez-Lozano/Billiard-dataset/blob/main/example.png?raw=true)

## How to cite this
More information about the aim of our work can be found in our paper. If you use this dataset, make sure you cite this work as:
```latex
@article{Rodriguez-Lozano-3DBILLIARDMOLT_2022,
	author = {Rodriguez-Lozano, Francisco J. and Gámez-Granados, Juan C. and León-García, Fernando and Palomares, Jose M. and Olivares, J.},
	title = {3D reconstruction system and multi-object local tracking algorithm designed for billiards},
 	year = {2022},
	month = {-},
	publisher = {-},
	volume = {-},
	number = {-},
	journal = {-},
	doi = {-},
	url = {-},
}
```
## Dataset link
The dataset requires approximately 190 GB of disk space, and it is available at the following web link:[Link](ENLACE a OneDRIVE)

## Dataset content
The data set includes: 100 recordings of shots made in the blackball billiard modality; 100 recordings of shots in the carom billiard modality; 100 recordings of shots in the snooker billiard modality. In addition, not only are these recordings available, but the exact positions have been obtained manually for a subset of each modality, carrying out comparisons with different methodologies and with the algorithm proposed in our work. Therefore, in the dataset we can find the following folders and files: 

* **blackball**: 
	* **blackball_[0...to...99]**: subfolders of each recording of the blackball billiard modality.
		* *BGR.dat*: raw data of the recording. A special function is required to display it (see *"How to read 'BGR.dat' raw data" section*). 
		* *BGR.avi*: rendered video from BGR.dat with compression.
		* *AnimationsResults*: subfolder with the 3D virtual generated worlds. It contains the animation files in ".x3d" format and rendered in video with format ".avi" with compression.  
		* *TrackingResults*: subfolder with the results of all the tested algorithms. It contains "_track.png" images with the trajectories retrieved by each algorithm, and rendered videos comparing each algorithm. 
	*  **background.png**: a background image of the table without balls or external elements, in case any user needs to use it. 
	*  **floderIndex.txt**: A list of available subfolders. 
* **BlackBall_Manual**:
 	*  **BlackBall_Manual_[0...to...21]**: subfolders of each recording of the blackball billiard modality.* This subfolder has inside the manual trajectory of the shot.
		* *BGR.dat*: raw data of the recording. A special function is required to display it (see *"How to read 'BGR.dat' raw data" section*). 
		* *BGR.avi*: rendered video from BGR.dat with compression.
		* *Jaccard_Coefficient.txt*: a file that contains the results of the Jaccard index for each algorithm.
		* *manual_track.png*: the ground truth trajectories of each object in movement.  
		* *AnimationsResults*: subfolder with the 3D virtual generated worlds. It contains the animation files in ".x3d" format and rendered in video with format ".avi" with compression.  
		* *TrackingResults*: subfolder with the results of all the tested algorithms. It contains "_track.png" images with the trajectories retrieved by each algorithm, "IOU_.png" images with the Intersection over the Union of the trajectories of each algorithm with the Manual trajectory. Also, rendered videos comparing each algorithm are available. 
	*  **background.png**: a background image of the table without balls or external elements, in case any user needs to use it. 
	*  **floderIndex.txt**: A list of available subfolders. 
	*  **Jaccard_Coefficient_Average.txt**: an average of the results for each algorithm compared using the Jaccard index for the folders available in the file "folderIndex.txt".
* **carom**:
	*  **carom_[0...to...99]**: subfolders of each recording of the carom billiard modality.
		* *BGR.dat*: raw data of the recording. A special function is required to display it (see *"How to read 'BGR.dat' raw data" section*). 
		* *BGR.avi*: rendered video from BGR.dat with compression.
		* *AnimationsResults*: subfolder with the 3D virtual generated worlds. It contains the animation files in ".x3d" format and rendered in video with format ".avi" with compression.  
		* *TrackingResults*: subfolder with the results of all the tested algorithms. It contains "_track.png" images with the trajectories retrieved by each algorithm, and rendered videos comparing each algorithm. 
	*  **background.png**: a background image of the table without balls or external elements, in case any user needs to use it. 
	*  **floderIndex.txt**: A list of available subfolders. 
* **Carom_Manual**:
 	*  **Carom_Manual_[0...to...15]**: subfolders of each recording of the carom billiard modality.* This subfolder has inside the manual trajectory of the shot.
		* *BGR.dat*: raw data of the recording. A special function is required to display it (see *"How to read 'BGR.dat' raw data" section*). 
		* *BGR.avi*: rendered video from BGR.dat with compression.
		* *Jaccard_Coefficient.txt*: a file that contains the results of the Jaccard index for each algorithm.
		* *manual_track.png*: the ground truth trajectories of each object in movement.  
		* *AnimationsResults*: subfolder with the 3D virtual generated worlds. It contains the animation files in ".x3d" format and rendered in video with format ".avi" with compression.  
		* *TrackingResults*: subfolder with the results of all the tested algorithms. It contains "_track.png" images with the trajectories retrieved by each algorithm, "IOU_.png" images with the Intersection over the Union of the trajectories of each algorithm with the Manual trajectory. Also, rendered videos comparing each algorithm are available. 
	*  **background.png**: a background image of the table without balls or external elements, in case any user needs to use it. 
	*  **floderIndex.txt**: A list of available subfolders. 
	*  **Jaccard_Coefficient_Average.txt**: an average of the results for each algorithm compared using the Jaccard index for the folders available in the file "folderIndex.txt".
* **snooker**:
	*  **snooker_[0...to...99]**: subfolders of each recording of the snooker billiard modality.
		* *BGR.dat*: raw data of the recording. A special function is required to display it (see *"How to read 'BGR.dat' raw data" section*). 
		* *BGR.avi*: rendered video from BGR.dat with compression.
		* *AnimationsResults*: subfolder with the 3D virtual generated worlds. It contains the animation files in ".x3d" format and rendered in video with format ".avi" with compression.  
		* *TrackingResults*: subfolder with the results of all the tested algorithms. It contains "_track.png" images with the trajectories retrieved by each algorithm, and rendered videos comparing each algorithm. 
	*  **background.png**: a background image of the table without balls or external elements, in case any user needs to use it. 
	*  **floderIndex.txt**: A list of available subfolders. 
* **Snooker_Manual**:
 	*  **nooker_Manual_[0...to...15]**: subfolders of each recording of the snooker billiard modality.* This subfolder has inside the manual trajectory of the shot.
		* *BGR.dat*: raw data of the recording. A special function is required to display it (see *"How to read 'BGR.dat' raw data" section*). 
		* *BGR.avi*: rendered video from BGR.dat with compression.
		* *Jaccard_Coefficient.txt*: a file that contains the results of the Jaccard index for each algorithm.
		* *manual_track.png*: the ground truth trajectories of each object in movement.  
		* *AnimationsResults*: subfolder with the 3D virtual generated worlds. It contains the animation files in ".x3d" format and rendered in video with format ".avi" with compression.  
		* *TrackingResults*: subfolder with the results of all the tested algorithms. It contains "_track.png" images with the trajectories retrieved by each algorithm, "IOU_.png" images with the Intersection over the Union of the trajectories of each algorithm with the Manual trajectory. Also, rendered videos comparing each algorithm are available. 
	*  **background.png**: a background image of the table without balls or external elements, in case any user needs to use it. 
	*  **floderIndex.txt**: A list of available subfolders. 
	*  **Jaccard_Coefficient_Average.txt**: an average of the results for each algorithm compared using the Jaccard index for the folders available in the file "folderIndex.txt". 


### How to read 'BGR.dat' raw data
If the user wishes to use the original raw data (BGR.dat), he must adapt the following code to the specific needs of his program: 
```cpp

#include <fstream>
#include <iostream>
#include <opencv2/opencv.hpp>

using namespace std;
using namespace cv;

/*Function used to read the raw "BGR.dat" files using OpenCV and C++ */
int readMatFromFile(ifstream& input, Mat &Img)
{
int matCols = Img.cols, matRows = Img.rows;
int type = Img.type();
int cont=0, cont2=0;

Vec3b value;

  switch (type)
  {
    case CV_8UC3:
      for (cont=0; cont < matRows; ++cont)
      {
        for (cont2=0; cont2 < matCols; ++cont2)
        {  
          input.read((char*) &value, sizeof(value));
          Img.at<Vec3b>(cont, cont2) = value;           
        }
      }
    break;
    // more cases to add
    default:
      cout << "Error: format not supported! Conrrently supported: CV_8UC3\n";
      return -1;
    break;
  }

return 0;
}

int main (int argc, char* argv[])
{
ifstream BGRimage;
bool goOut = false;

  imagenRGB.open(argv[1], ios::in|ios::binary);

  while(!goOut)
  {
    Mat image(480, 640, CV_8UC3);
    // reading of each frame
    readMatFromFile(imagenRGB, image);

    // do something with the image
    
    if(imagenRGB.eof())
      goOut = true;
  }
  
  imagenRGB.close;  

return 0;
}

```
## License
This dataset is licensed by the author under a CC BY-SA 4.0 license [https://creativecommons.org/licenses/by-sa/4.0/deed.en](https://creativecommons.org/licenses/by-sa/4.0/deed.en).
