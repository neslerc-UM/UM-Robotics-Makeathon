![Image](https://azurecomcdn.azureedge.net/cvt-bc3f4c4e6b646345d1c1a1425d51224d382a8510f86a16956356959c3dcdc834/images/page/services/azure-kinect-dk/health.jpg)

Image from Azure Kinect DK.

# Measuring Rehabilitation Outcomes from Video Recordings
For Prosthetists and Orthotists, it is important to measure objective rehabilitation outcomes to asses patient progress. These rehabilitation outcomes typically include specific metrics of the human lower-limb kinematics, such as step length, cadence, and Range of Motion (RoM) of the joints. These metrics are available using motion capture systems, e.g., using [Vicon](https://www.vicon.com/) or [XSens](https://www.xsens.com/). However, the cost of these systems makes these kind of analyses prohibitive for most clinicians. **The objective of this project is to create an open-source tool to analyse human lower-limb kinematics from RGB video and depth sensor recordings.** Fortunately, we can leverage the results from the [OpenPose](https://github.com/CMU-Perceptual-Computing-Lab/openpose) project to materialize this objective!
# The challenge
## Easy
* Estimate ROM of the knee and ankle joints from a video recording. Offline or real-time estimation is valid.
* Auto-generate a pdf file that reports the mean, median, maximum, and minimum ROM for each joint for the complete length of the video.
* Provide uncertainty of every measurement.

## Medium (includes objectives at easy level)
* Calculate the step length and cadence.
* Include the mean, median, maximum, and minimum step lengths and cadences in the pdf report.
* Include a plot of the joint angle vs. time for the knee and ankle joints. Select a time window that is easy for visualization and is representative of the data.
## Spicy (includes objectives at medium level)
* Fragment the joint angles of the knee and ankles in multiple time windows. Each time window should include exactly one gait cycle.
* Estimate the angle of the shank and thight with respect to the global vertical (Note: you may need to integrate the information from the Kinect IMU)
* Include a violin plot to report the statistics of the ROM, step length, and cadence.
* Create a real-time video that shows in parallel the motion of the patient with the skeleton from OpenPose, the joint angle vs. time for the knee and ankle, and the statistical information from the the data currently in display.

# Example
![Image](LiveData_automaticTracking_B-2.gif)

GIF from Dartfish.
# Resources
1. You will have access to an [Azure Kinect DK.](https://azure.microsoft.com/en-us/services/kinect-dk/)
1. [OpenPose.](https://github.com/CMU-Perceptual-Computing-Lab/openpose)
1. [Azure Kinect Body Tracking SDK.](https://docs.microsoft.com/en-us/azure/Kinect-dk/body-sdk-download)
1. [Dartfish](https://www.dartfish.com/healthcare). An example from industry.

# Desired skills
1. Experience or interest in learning C++
1. Exposure or interest in OpenCV
1. Interest in front-end development (optional)

# Constraints
1. Develop the tool for Windows 10/8. Our alpha test will be to deploy our tool at the UM-Orthotics and Prosthetic Center ([UMOPC](https://www.uofmhealth.org/our-locations/south-industrial-op)).  The UMOPC will have access only to Windows machines.
