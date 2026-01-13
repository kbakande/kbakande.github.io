---
layout: post
title: Towards the Google PMLE Certification
comments: true
---
<!-- ![Google-Ml-Engineer]({{ "assets/images/Google-Professional-Level-Background.png" | absolute_url }}){: .center-image } -->
![Google-Ml-Engineer](/assets/images/Google-Professional-Level-Background.png)
# Prelude
The Google professional machine learning engineer (PMLE) certification is a suitable target for those who need to stay motivated while learning the various machine learning services offered on Google cloud platform (GCP). It is also one of a number of ways to demonstrate GCP expertise to potential employers. While the jury is out on the real worth of tech certifications in general,  at the very least, it should lead to potentially more interviews for those actively seeking employment. 

# Path to Google PMLE Certification
Preparing for Google PMLE can be frustrating due to the required depth and breadth of the resources. However, depending on your experience, you might only need to focus on certain areas especially if you are actively practising. I will advise would-be exam takers to first try out Google [sample questions](https://docs.google.com/forms/d/e/1FAIpQLSeYmkCANE81qSBqLW0g2X7RoskBX9yGYQu-m1TtsjMvHabGqg/viewform){:target="_blank"} in order to have a taste of the real exam flavour. I found the reasonings and logics in the answers very useful and it is something one would need to develop and sharpen to be comfortable in the exam. Due to the fact that I use GCP in my work on daily basis, I mostly focus on the summaries and assessments on many of the available resources during my preparation for the exam. 

# Fundamentals
While practising for the exam, I noticed some patterns which I further develop into effective strategies for answering many of the exam questions. There are three main areas tested in the certification. The first part tests fundamentals of machine learning and data science knowledge with questions bordering on data preparation, modelling techniques, model performance and monitoring metrics, retraining and so on. The second part tests the knowledge of various GCP products while the last part of the exam tests the candidate's ability to choose the best combination of GCP products based on the presented scenario. The selection parameters/criteria that frequently come up in the exam scenarios are cost, data size, latency, speed/time, scalability, customisation and infrastructure maintenance. I have illustrated these criteria with some examples.
 * Cost: Google Vertex AI is costlier than Kubeflow since the former is a fully managed service while the latter is not. However, the required infrastructure maintenance effort is more in kubeflow but that also means more control over customisation. 
 * Speed: GPUs are recommended for high precision deep learning training but if time is not of the essence and the application can afford low precision, TPUs are preffered.
 * Scalability: Notebook offers a platform for quick experimentation but would not scale with increasing number of hyperparameters and associated search space. Hence, there would be need to migrate code from notebook to container to take advantage of parallel processing and automation.

This same consideration underpins other tools selections such as Dataproc, Dataprep, Dataflow and Data studio as well as pipelining frameworks.

# Format and Structure
The Google PMLE is a two-hour multiple-choice exam that can be taken both onsite and online. I chose the online option as it is the most conveneient for me. For the succesful conduct of the online version, the onus is on the exam taker to ensure their laptop meets all the specified requirements as stated on the proctoring site. There were checks prior to the exam commencement around the exam surroundings, it is aptly reffered to as *securing the test site* which clearly sounds like some top-secret military operation. The exam taker is not allowed any break within the exam and if eyes stray away from the screen for a little while, a warning flashed up on the screen urging the exam taker to focus on the screen. Goodluck to some poor guys trying to cheat Google. It was mentally draining for me especially towards the tail end of the exam so my advice would be to ensure adequate mental preparation prior to taking the exam.

# Resources
I have curated the resources I found most helpful for the certification as follows: 

1. Google [machine learning crash course](https://developers.google.com/machine-learning/crash-course) is a useful resource to study, even for an experienced practitioner. 
2. Google [machine learning engineer learning path](https://www.cloudskillsboost.google/paths/17) is a comprehensive collection of courses which needs a lot of time and dedication. If you dont have time to study the courses, you can skip to the summary and assessment at the end of each course which is mostly what I did. 
3. [Journey-Become-Machine-Learning-Engineer](https://www.amazon.com/Journey-Become-Machine-Learning-Engineer/dp/1803233729) seems the only book available at the moment and is a good read as it covers many of the topics in the certification with some sample questions.
4. [Curated resources](https://github.com/sathishvj/awesome-gcp-certifications/blob/master/professional-machine-learning-engineer.md) is a one stop place for all things related to Google PMLE certification.
5. This [Blog](https://dzlab.github.io/certification/2022/01/08/gcp-ml-engineer-prep/) is a comprehensive overview of the exam key areas along with corresponding links. It is probably sufficient on its own for an experienced practitioner.
6. [Coursera](https://gb.coursera.org/professional-certificates/preparing-for-google-cloud-machine-learning-engineer-professional-certificate) also has a specialisation course which seems a repetition of what is available on Google learning path but might be easier to follow.

I hope the info helps you in your journey towards acquiring the Google PMLE and wish you success in your quest.

