# CWT Analysis Script

This is the documentation describing how to use the script to convert trust submission data into CWT adherence data.

## Dependencies

In order to run the script, you will need to install additional software on your machine. In total, the dependencies are:

* Jupyter Notebook
* Python 3
* pandas 0.20

 The easiest way to install all of these dependecies is by simply installing the anaconda data science package, which includes all of the above. It can be found under this [link](https://www.anaconda.com/download/)
 
## Getting Started

In order to get started you will need to extract the zip file containing the script into your desired location. 

Following you will need to launch an instance of a jupyter notebook, which runs the actual script.

You can find more information here, but these are the basics:

1. open your command line and navigate to where you extracted the zip file
2. in your command line, type the command `jupyter notebook`
3. A browser window will open that shows the interface of the jupyter notebook. Open the CWT transformation script

## Using the Script

The script is commented and hence should be self explanatory. In order to transform new data, just change the data source file in the location specified. 

The script automatically produces a CSV and JSON output. These will be saved next to the files you extracted earlier.

## Importing data into the imrsv.data application

In order to get the data into the Hololens app, you only need to save the exported CSV / JSON (both will work) in the one drive folder that is connected to your Hololens. You can then open the file on the application itself using the one drive file picker (this needs to be installed on the hololens - see the imrsv.data [documentation](https://lucasvaltl.github.io/imrsv.data-documentation/#/?id=user-manual) for more details)

## Description of Output

The output is described as follows:

| month                                            | Categorical | Month of occurrence                                                                                  |
|--------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------|
| shared_breach                                    | Boolean     | 1: if a shared treatment and breached, 0 if shared treatment but not breached                        |
| urgent\_value_2ww                                 | Float       | Length of urgent 2 week wait time                                                                    |
| urgent\_breach_2ww                                | Boolean     | Adherence to urgent 2 week wait time: 1 if breached, 0 if not                                        |
| breast\_value_2ww                                 | Float       | Length of 2 week wait  time for suspected breast cancer                                              |
| breast\_breach_2ww                                | Boolean     | Adherence to 2 week wait  time for suspected breast cancer: 1 if breached, 0 if not                  |
| first\_treatment\_value_31d                        | Float       | Length of 31 days wait time (first treatment)                                                        |
| first\_treatment\_breach_31d                       | Boolean     | Adherence to 31 days wait time (first treatment): 1 if breached, 0 if not                            |
| subsequent\_treatment\_radio\_or\_surgery\_value_31d  | Float       | Length of 31 days wait time (subsequent treatment with radio or surgery)                             |
| subsequent\_treatment_radio\_or\_surgery\_breach\_31d | Boolean     | Adherence to 31 days wait time (subsequent treatment with radio or surgery): 1 if breached, 0 if not |
| subsequent\_treatment\_chemo\_value_31d             | Float       | Length of 31 days wait time (subsequent treatment with chemotherapy)                                 |
| subsequent\_treatment\_chemo\_breach_31d            | Boolean     | Adherence to 31 days wait time (subsequent treatment with chemotherapy): 1 if breached, 0 if not     |
| regular\_value_62d                                | Float       | Length of 62 day wait category                                                                       |
| regular\_breach_62d                               | Boolean     | Adherence to 62 day wait category: 1 if breached, 0 if not                                           |
| from\_screenprograms\_value_62d                    | Float       | Length of 62 day wait category coming from NHS screening programs                                    |
| from\_screenprograms\_breach_62d                   | Boolean     | Adherence to 62 day wait category coming from NHS screening programs: 1 if breached, 0 if not        |
| cancer\_treatment\_modality_type                   | Categorical | Type of treatment modality                                                                           |
| cancer\_treatment\_modality\_sub\_treatment\_group    | Categorical | Type of sub treatment group                                                                          |
| diagnosis\_reporting_category                     | Categorical | Type of diagnosis                                                                                    |
| provider\_date\_first\_seen_name                    | Categorical | Referring provider if shared treatment               
