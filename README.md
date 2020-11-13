# OpenCV-Computer-vision

Load and display an image using OpenCV---------











#include<opencv2/opencv.hpp>//header file of opencv
#include<iostream>
using namespace std;
using namespace cv;//compulsory syntax for c++
int main() {
	Mat image = imread("C:/Users/Bhawuk Khurana/Downloads/vision-hw0-master/data/dog.jpg");//function to load an image
	//If the function cannot read the file, it will return an empty Mat object.
  // Check for failure,if no file is there
	if (image.empty())
	{
		cout << "Could not open or find the image" << endl;
		cin.get(); //wait for any key press
		return -1;
	}
	
	//Add a window for display of image
	String windowName = "Bhawuk1";//Give a name to window

	namedWindow(windowName);//create a window

	imshow(windowName, image);//show your image inside your created window

	waitKey(0); // Wait for any keystroke in the window.When any key is pressed, this function returns the ASCII value of the key and your program will continue
	//This function only works if there is at least one active HIGHGUI window opened by the program.
       destroyWindow(windowName); //destroy the created window.Not so important
return 0;
}
