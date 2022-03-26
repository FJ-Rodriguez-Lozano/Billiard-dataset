# Billiard-dataset
Billiard recording dataset for blackball, carom billiard, and snooker. Raw data and results from research paper titled: "3D reconstruction system and multi-object local tracking algorithm designed for billiards"

---
int readMatFromFile(ifstream& in, Mat &I){

int matCols = I.cols, matRows = I.rows; // Lectura de los datos de la imagen.
int type = I.type(); //Lectura del tipo de dato de la imagen.
int cont=0, cont2=0; // Contadores para recorrer las filas y columnas de la imagen.

Vec3b fvalue; // Tipo de dato para imágenes de tres canales.
unsigned short dvalue; // Tipo de dato para imágenes de un canal.

  switch (type)
  {
    case CV_8UC3: // Caso de imagen de tres canales.
      for (cont=0; cont < matRows; ++cont)
      {
        for (cont2=0; cont2 < matCols; ++cont2)
        {  
          in.read((char*) &fvalue, sizeof(fvalue));
          I.at<Vec3b>(cont, cont2) = fvalue;           
        }
      }
    break;
    
    case CV_16UC1: // Caso de imagen de un canal.
      for (cont=0; cont < matRows; ++cont)
      {
        for (cont2=0; cont2 < matCols; ++cont2)
        {  
          in.read((char*) &dvalue, sizeof(dvalue));
          I.at<unsigned short>(cont, cont2) = dvalue;
        }
      }
    break;

    default: // Cualquier otro tipo no definido.
      cout << "Error: formato no admitido, por ahora solo están implementados los tipos: CV_8UC3, CV_16UC1\n";
      return -1;
    break;
  }

return 0;
}
  ---
