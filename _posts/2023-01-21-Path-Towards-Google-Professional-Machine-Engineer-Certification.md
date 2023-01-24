---
layout: post
title: Towards the Google PMLE Certification
---
<!-- ![Google-Ml-Engineer]({{ "assets/images/Google-Professional-Level-Background.png" | absolute_url }}){: .center-image } -->
![Google-Ml-Engineer](/assets/images/Google-Professional-Level-Background.png)
# Prelude
The Google professional machine learning engineer (PMLE) certification is a suitable target for those who need to stay motivated while learning the various machine learning services offered on Google cloud platform (GCP). It is also one of a number of ways to demonstrate GCP expertise to potential employers. While the jury is out on the real worth of tech certifications in general,  at the very least, it should lead to potentially more interviews for those actively seeking employment. 

# Path to PMLE Certification
Preparing for Google PMLE can be frustrating due to the required depth and breadth of the resources. However, depending on your experience, you might only need to focus on certain areas especially if you are actively practising. I will advise would-be exam takers to first try out Google [sample questions](https://docs.google.com/forms/d/e/1FAIpQLSeYmkCANE81qSBqLW0g2X7RoskBX9yGYQu-m1TtsjMvHabGqg/viewform){:target="_blank"} to have a taste of the real exam flavour. I found the reasonings and logics in the answers very useful and it is something one would need to develop and sharpen to be comfortable in the exam. Due to the fact that I use GCP in my work on daily basis, I mostly focus on the summaries and assessments on many of the available resources. 

# Fundamentals
While practising for the exam, I noticed some patterns which I further develop into effective strategies for answering many of the questions. Though some part of the exam test the fundamentals of machine learning and data science knowledge, the core of the exam tests the candidate's ability to choose the best GCP tools combination based on the presented scenario. So it is mostly knowing tools combination that fits the best practises for machine learning flow on the GCP as opposed to testing the knowledge of specific GCP tools. The selection parameters/criteria that frequently come up are cost, data size, latency, time, duration (short time vs long time), customisation and infrastructure maintenance. I have illustrated these criteria with some examples.
 * Cost : Google Vertex AI is costlier than Kubeflow since the former is a fully managed service while the latter is not. However, the required infrastruture maintenance effort is more in kubeflow which translates to more lower level control. So a scenario depicting available expertise and 
 * Customisation: AUTOML offers quick modelling path but with less customisation compared to custom built models and this cut across tabular, text and image data modelling.
 * Time: Notebooks offers a platform for quick exprrimentation but  

This same consideration underpins other tools selections such as Dataproc, Dataprep, Dataflow and Data studio as well as pipelining frameworks.

# Format and Structure
The Google PMLE is a two hour multiple choice exam that can be taken both onsite and online. I chose the online option as it is most conveneient for me. For the succesful conduct of the online version, the onus is on the exam taker to ensure the laptop meet all the specified requirement as stated on the proctoring site. There were checks prior to the exam commencement around the exam surroundings, it is aptly reffered to as *securing the test site* which clearly sound like some top secret military operations. The exam taker is not allowed any break within the exam and if eyes stray away from the screen for a little while, a warning falshed up on the screen urging the exam taker to focus on the screen. Goodluck to some poor guys trying to cheat Google. The advise 

# Resources
I have curated the resources as follows: 

1. Google [machine learning crash course](https://developers.google.com/machine-learning/crash-course) is a resource to study even for an experienced practitioner. 
2. Google [Machine Learning Engineer Learning Path](https://www.cloudskillsboost.google/paths/17) is a comprehensive collection of courses which needs a lot of time. If you dont have to study the courses, you can skip to the summary and assessment at the end of each course which is mostly what I did. 
3. [Journey-Become-Machine-Learning-Engineer](https://www.amazon.com/Journey-Become-Machine-Learning-Engineer/dp/1803233729Book) seems the only book available at the moment and is a good read as it covers many of the topics in the certification.
4. [Curated resources](https://github.com/sathishvj/awesome-gcp-certifications/blob/master/professional-machine-learning-engineer.md) is a one stop place for all things related to GPMLE certification
5. [Blog](https://dzlab.github.io/certification/2022/01/08/gcp-ml-engineer-prep/) is a comprehensive overview of the exam key areas along with corresponding links. It is probably suficient on its own for an experienced practitioner
6. [Coursera](https://gb.coursera.org/professional-certificates/preparing-for-google-cloud-machine-learning-engineer-professional-certificate) also has a course which seems a repetition what is available on Google learning path but might be easier to follow.


