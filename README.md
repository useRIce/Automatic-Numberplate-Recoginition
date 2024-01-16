# Automatic-number-plate-recognition-python-yolov8

## Important:
1) Python ver **3.8.10** was used and Python ver 3.8 - 3.9 is recommended as using any other version might lead to issues regarding python 3rd party package dependencies.

2) The 3rd party python packages used are already incorporated in the virtual environment (venv/) and are further listed in requirements.txt

## Dataset (not in repo)
1) Dataset (Indian number plate) used to train the models are listed <a href="https://www.kaggle.com/datasets/deepakat002/indian-vehicle-number-plate-yolo-annotation?resource=download">here</a>.
And the trained model is present in directory:
> runs\detect\train3\weights\best.pt
This model (Indian number plate ds)  is best among the 3 (train. train2 and train3)

3) For UK Number plate dataset visit <a href="https://universe.roboflow.com/roboflow-universe-projects/license-plate-recognition-rxg4e/dataset/4">here</a> and train this dataset using command:
> yolo detect train data=config.yaml model="yolov8n.yaml" epochs='' imgsz=640

## Running and usage
There are 4 .py files out of which only 3 (main.py, add_missing_data.py and visualize.py) are used to execute numper plate detection. The role of the 3 files are as follows:-

1) main.py --> main program to detect and list all the detection in form of CSV file (here, test.csv). The specification of the test.csv are written in last comment of the main.py.
(**Creates test.csv file**)

2) add_missing_data.py --> interpolates the CSV file (test.csv) to create a CSV file (test_interpolated.csv) to cover the mid frame detection issue.
(**Creates test_interpolated.csv file using test.csv file**)

4) visualize.py --> outputes a video file (out.mp4) that contains bounding box diagram for both number plate and respective car.
(**Creates out.mp4 file**)

## Issues
If you get issues downloading lap ver 0.4.0 package using requirements.txt , remove it from the text file and save and try installing again.
Also, this repo might not contain all the LICENCES or mentions.