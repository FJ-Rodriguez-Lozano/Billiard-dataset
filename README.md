# Billiard-dataset
Billiard-dataset is a collection of recordings made for the scientific paper titled: "3D reconstruction system and multi-object local tracking algorithm designed for billiards". The main objective is the creation of a system to perform a reconstruction of billiards moves in a 3D virtual world and a new multi-object tracking algorithm applied to billiards. More information about the aim of our work can be found in our paper. If you use this dataset, make sure you cite this work as:
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
The data set includes: 100 recordings of shots made in the blackball billiard modality; 100 recordings of shots in the carom billiard modality; 100 recordings of shots in the snooker billiard modality. In addition, not only are these recordings available, but the exact positions have been obtained manually for a subset of each modality, carrying out comparisons with different methodologies and with the algorithm proposed in our work. These subsets are found inside the folders: "BlackBall_Manual", "Carom_Manual", and "Snooker_Manual".


```cpp
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

```
