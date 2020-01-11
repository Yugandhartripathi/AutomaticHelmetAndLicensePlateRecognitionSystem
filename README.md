# AutomaticHelmetAndLicensePlateRecognitionSystem
## How it works:

Video traffic data is passed through following stages: 
1) Frame selection based on various heuristics
2) Then the select frame is passed to first model to detect bike and extract region of interest(which is temporarily saved) based on defined heuristics
3) Then the extracted region goes into another model for Helmet detection and extraction of helmet region(which is temporarily saved)
4) Now,<br>
if (helmet is detected):<br>
&nbsp;&nbsp;then the bike ROI is passed to third model for License plate detection and extraction which is then saved into a csv with previously saved proofs of violation.<br>
else:<br>
&nbsp;&nbsp;All data previously saved is removed and the process control goes back to stage 1.
