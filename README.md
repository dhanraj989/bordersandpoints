
----
All the functions in this repository can be imported using can be import using pip: 

----
```
pip install torch torchvision
pip install -U git+https://github.com/luca-medeiros/lang-segment-anything.git
pip install bordersandpoints
```
----
You can also clone this repo and install the library:

----
```
git clone https://github.com/dhanraj989/bordersandpoints.git
```
change directory to location where this repository is cloned
```
cd ./bordersandpoints
```
Then using pip install the following:  
```
pip install "dist/bordersandpoints-1.1.0-py3-none-any.whl"
```
----
**Image containing usage of the library:**

----
![bordersandpoints drawio](https://github.com/dhanraj989/bordersandpoints/assets/75594686/6037b10c-2afe-4976-834f-dfe0aaecba02)  

----

**Information related to functions in the library:**

----
* After importing the library, there are three functions border_lines_cap,create_video,process_video:
* **process_video(video_file,video_path,output_path,initial_point):** This function uses farneback algorithm and outputs a video tracking point which is continuously present in a 2D tree trunk video.
  video_file: list containing name of the files in the folder
  video_path: path of the folder containing files in video_files
  output_path: path of the output folder
  initial_point: point which you want to track
* **border_lines_cap(video_file,frames_path, lines_output):** This function outputs borders for each frame in input video file
  video_file: list containing name of the files in the folder
  output_path: path of the folder containing files in video_files
  lines_output: path of the output folder
* **create_video(lines_output, output_file_path):** This function outputs video by taking frames as input
  lines_ouput: list containing name of the files in the folder
  output_file_path: path in which output file to be stored

----
**Steps to be followed to add border lines and tracking a point which is continuously present in a 2D tree trunk video:**  

----
* First use the process_video function and get the video with point tracked
* Then use border_lines_cap function with output video file from process_function as input
* Lastly, use create_video function to get video from the video frames output from border_lines_cap function

----
**Example usage:**

----
* An example usage ipynb file is attached in ./usage_example folder to get video with border lines and tracking a point which is continuously present in a 2D tree trunk video
* I have used Kaggle GPU, but if anyone wants to run on their system then linux subsystem is required for windows users

----

**Results along with Example Input and Output**

----
* Procured an average distance between the border lines of 2.36 and RMSE score of 0.53 for detecting continuous point positions
Here is an example input video converted to GIF:  
![Untitled video - Made with Clipchamp (1)](https://github.com/dhanraj989/bordersandpoints/assets/75594686/d1706be6-71a8-47e3-893a-8fdce289164d)

Corresponding output video converted to GIF:  
![Untitled video - Made with Clipchamp](https://github.com/dhanraj989/bordersandpoints/assets/75594686/bf4a157f-d700-463a-ae63-469e80c07a3c)

----
**Files in this repository**

----
* **usage_example folder:** Contains an ipynb file which has example usage of the library. This folder also contains the input video file used in the ipynb file and the final output video obtained after running the ipynb file
* **bordersandpoints folder:** This folder contains 'border_lines.py' python file which has functions contained in the bordersandpoints library
