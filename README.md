# Billiard-dataset
Billiard recording dataset for blackball, carom billiard, and snooker. Raw data and results from research paper titled: "3D reconstruction system and multi-object local tracking algorithm designed for billiards"


More information about the dataset can be found in our paper. If you use this dataset, make sure you cite this work as:
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
