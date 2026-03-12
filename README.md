# SVAD-Dataset
A weakly-labeled video anomaly deterction dataset with five novel anomaly types, providing both closed-set and open-set splits.

## Data Collection and Annotation
Most mainstream video anomaly detection datasets focus on road events and violence-related scenarios. However, as short videos with diverse backgrounds and events become a popular entertainment way, the video anomaly detection task has become increasingly challenging. This trend highlights an urgent need for more comprehensive anomaly types to train models that are more adaptable to real-world detection. 

For this reason, we collected **383** short videos from mainstream video websites, including **193** normal videos and **190** abnormal videos. There are some samples in the following figure. The SVAD dataset has a total of **225172** frames, including **188136** normal frames and **37038** abnormal frames.  

<img width="1895" height="1650" alt="Figs_SVAD_samples" src="https://github.com/user-attachments/assets/54b0202e-ca9a-4c41-b5f4-497ebcc29ffd" />

We divided it into seven anomaly types: **Animal Abuse, Animal Killing, Carnie Accident, Accidental Hurt, Traffic Accident, Fights and Falling Accident**. The detailed statistics of the categories in the following table. And we provide frame-level annotations for every abnormal video, labeling the start and end frames of every anomaly segment. For frame-level annotation, we only label the start and end frames of anomalous segments for abnormal samples in the SVAD dataset.

<img width="510" height="318" alt="Table_categories of the SVAD" src="https://github.com/user-attachments/assets/fdc55adf-b6b1-46fa-aab6-06548bb7f82e" />

## Data Split

To train the detection models rigorously, the SVAD dataset performs both closed-set and open-set tasks. In the closed-set split, we set the ratio of training to testing set as 7:3, which is randomly selected in each category. For the open-set split, we select four anomaly categories **(Animal Abuse, Carine Accident, Falling Accident, Fights**) and randomly select half of the normal categories as the training set; we select the remaining three anomaly categories **(Animal Killing, Accidental Hurt, Traffic Accident)** and the other half of the normal categories as the test set. The abnormal categories in the training set cover accidental and violent events involving animals and humans as the main subjects, enabling the model to acquire basic knowledge of the real world. In contrast, the abnormal categories in the test set are semantically similar to those in the training set yet more extensive — for instance, evolving from Animal Abuse to the more complex act of Animal Killing, and from typical accidental events such as Falling to various types of unintentional injuries. This design can effectively evaluate the generalization ability of the trained model to real-world scenarios. Detailed information in our split is in the following table. 

<img width="449" height="253" alt="Table_splits of the SVAD" src="https://github.com/user-attachments/assets/4e60d06a-fba5-4c88-8df2-785579f7c1d6" />

## Dataset Ethics, Compliance, and Accessibility

Our dataset is entirely constructed from publicly accessible video resources. All data collection activities strictly adhere to the terms of service and copyright regulations of each platform. Access to the dataset is restricted to academic research purposes exclusively. The dataset does not contain high-resolution facial images or identifiable personal information. All content involving personal privacy has undergone appropriate anonymization. We are committed to upholding privacy protection and ethical compliance, ensuring no violations of privacy regulations in the dataset's usage.

Moreover, it is worth emphasizing that our SVAD dataset has passed the Ethics Review Request of our university, and the form is attached to the submission materials. All data originates from public platforms that implement rigorous pre-publication content review mechanisms to ensure compliance with legal standards, copyright regulations, and community guidelines. Platforms including YouTube, Bilibili, and Douyin screen all uploaded videos to eliminate illegal, infringing, or non-compliant content. Consequently, the videos in our dataset have undergone these platform review processes and meet legal and ethical requirements.

 **To obtain the SVAD dataset, the applicants have to submit two application forms: Data Usage Application Form and Data Security Usage Commitment (listed in the github repository) to our email (address: 2212391069@st.gxu.edu.cn).**
