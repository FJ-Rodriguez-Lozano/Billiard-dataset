# Billiard-dataset
Billiard recording dataset for blackball, carom billiard, and snooker. Raw data and results from research paper titled: "3D reconstruction system and multi-object local tracking algorithm designed for billiards"

---
int readMatFromFile(ifstream& in, Mat &Img){

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
          in.read((char*) &value, sizeof(value));
          Img.at<Vec3b>(cont, cont2) = value;           
        }
      }
    break;
    // more cases to add
    default: // Cualquier otro tipo no definido.
      cout << "Error: format not supported! Conrrently supported: CV_8UC3\n";
      return -1;
    break;
  }

return 0;
}
  ---
