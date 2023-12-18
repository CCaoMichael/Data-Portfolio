# Comparing OpenAI Whisper and Zoom Transcription
This repository is one that was created in order to compare OpenAI Whisper, a speech-to-text service hosted by OpenAI, and the auto-generated transcriptions that Zoom provides for recordings. We used natural language processing techniques, including cosine similarity and n-grams, and AWS. Within AWS, weused Sagemaker, Boto3, S3 buckets, and the Whisper ML API to perform this comparative analysis between OpenAI's Whisper and Zoom's speech-to-text transcription services.

# Data and Further Applications
Though the data collected for this project falls squarely in the category of Machine Learning lecture recordings and is smaller in scale due to limited availability, the methods used here are broadly applicable to any audio recording where a comparison transcription is available.

# Architectural Diagram
![](https://github.com/CCaoMichael/Data-Portfolio/blob/289de7b5472d5e33b3717af1126d335354f889a9/Comparing%20OpenAI%20Whisper%20and%20Zoom%20Transcriptions/Misc/Architectural%20Diagram.png)
First, we acquired two Zoom recordings from a professor lecturing on machine learning. The topics of these lectures included LDA/QDA and Regularization/Selection. Following this, we converted the lecture recordings into mp3 files using an mp4 to mp3 converter online. Next, we downloaded the Zoom transcriptions from the posted video recordings.

In acquiring the Whisper transcript, we used AWS Sagemaker. We first stored our Zoom mp3 files into an s3 bucket. An s3 bucket is a public cloud storage container for objects stored in a simple storage service (s3). Next, we used Python boto3 to access our mp3 files stored in s3 buckets to utilize OpenAI. Boto3 is the Python SDK for AWS that allows you to directly create, update, and delete AWS resources from your Python scripts. After this, we used the OpenAI machine learning model to transcribe our Zoom mp3 files. Lastly, we stored the Zoom and OpenAI Whisper text transcriptions in a transcription bucket. From here, we used Python to perform our comparison.

# Reproduce
