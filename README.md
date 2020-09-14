# Skin-Lesion-Segmentation
## Python deep learning code fore skin lesion segmentation 

This code is written for the challenge of diagnosing skin disease, which is one of the biggest challenges of artificial intelligence in the field of medicine. For more information about this challenge, you can refer to the following link: https://www.kaggle.com/c/ima205challenge



**Introduction**

A skin lesion is defined as a superficial growth or patch of the skin that is visually different and/or has a different texture than its surrounding area. Skin lesions, such as moles or birthmarks, can degenerate and become melanoma, one of the deadliest skin cancer. Its incidence has been increasing during the last decades, especially in the areas mostly populated by white people.

The most effective treatment is an early detection followed by surgical excision. This is why several approaches for melanoma detection have been proposed in the last years (non-invasive computer-aided diagnosis (CAD) ).

**Goal of the challenge**

The goal of this challenge is to classify images of skin lesions as either benign or melanoma. In order to do that, you will extract features such as the Asymmetry, the Border irregularity, the Colour and the Dimension of the lesion (usually called the ABCD rule). After that, you will use machine learning algorithms to classify the images.

**Data**

The International Skin Imaging Collaboration (ISIC) is an international effort to improve melanoma diagnosis, sponsored by the International Society for Digital Imaging of the Skin (ISDIS). The ISIC Archive contains the largest publicly available collection of quality controlled dermoscopic images of skin lesions.

Presently, the ISIC Archive contains over 13,000 dermoscopic images, which were collected from leading clinical centers internationally and acquired from a variety of devices within each center. Broad and international participation in image contribution is designed to insure a representative clinically relevant sample.

All incoming images to the ISIC Archive are screened for both privacy and quality assurance. Most images have associated clinical metadata, which has been vetted by recognized melanoma experts. A subset of the images have undergone annotation and markup by recognized skin cancer experts. These markups include dermoscopic features (i.e., global and focal morphologic elements in the image known to discriminate between types of skin lesions). you can see some images of dataset below:


![alt text](https://storage.googleapis.com/kagglesdsdata/datasets%2F236015%2F502106%2Ftestx%2Fimgx1.jpg?GoogleAccessId=databundle-worker-v2@kaggle-161607.iam.gserviceaccount.com&Expires=1600270663&Signature=Eo9lQhIe3tUG0nkasvPdc6WMNAsD7rzDB8Y4axX2nvAMiDafudrREh1i0VVyNEIN%2BPSvngPa7DzcjHgfFYlD3s2h11FZLG0szRXR9FMAWwzeLiCgmF24ZBTv0E2UhfxkszxckeebJzfCrquIa6NCQW%2BA8jnEAwdiqSp24WWJxa3qoMO6413iVTRv9d6LDOx9m7szxEFMPcgh%2FWN%2BAoFMz%2Bdi0Shw6wiu%2B1ft4V41E9OGZl6F7V6VWZqVpmhQrimDVipCi2PaTR%2Bo%2BzUbyMh9aUQV8usJNZ4hKa3nQshwI2xjJiBwTcrUfkyzYNjvNPcE5W4cyynO3K7hnSdDW7pOqQ%3D%3D)
![alt text](https://storage.googleapis.com/kagglesdsdata/datasets%2F236015%2F502106%2Ftestx%2Fimgx11.jpg?GoogleAccessId=databundle-worker-v2@kaggle-161607.iam.gserviceaccount.com&Expires=1600270663&Signature=UmMsRxyGGKIZySu6tzlLUqf%2FYogYhlX8ACkV%2FxuboIJ54t0gKELYy2YPEDOq4vvhwSUdS2Za0U2zOZahbzp%2BpwxV%2BTuucRyaoS5Q%2F3iWOAqYl6DWu6Nh9K3nCmi%2FGfHG8dcxNmo9kihkeDOc6SDCKiMOkkPjyJ01mitQnFw1GEZkWcp2AnyjTS9QEJXoeBXRqOdR7OGeDzIUXQxbiof0%2BmATatT9WyDAvO6pm8szhVwqqIX1hB%2FMiTAQ6Vt0PoLec5HMNISblFT8PoSIKdQOacQe%2BhQLO%2F7Gz%2BcQMXKJlp04HFUVLalNLrgdUFO4vJz%2BQPDjU3IKxEX44hReYJrnxQ%3D%3D)
![alt text](https://storage.googleapis.com/kagglesdsdata/datasets%2F236015%2F502106%2Ftestx%2Fimgx116.jpg?GoogleAccessId=databundle-worker-v2@kaggle-161607.iam.gserviceaccount.com&Expires=1600270663&Signature=A6cYmJp7tkUSzqmDyhC9h5p3DkDCjd2EbnSph5t7sVPH0oP6dJ5BAYI0Q0fQaG5eKOKNIe8feHUNnVvGA1qPwvaseCeUVSVHmDazHnabMucXb7WJRXdqxHKRl8ROv2zLIfVznWPmxhSzqYXcHRPajSnL38O11zVnzhf1h%2Fc5kTk%2FIzVUNqqap1ybuc8q2FujRxA7%2B7QaIdjZ0SrKzomUO6BW4m5gkYNNgig1WURmB8%2BEeGNPPujIvrVT747kOCgPUfuiMswPXGB5H2ekkFIYHIvLz05o84DSRmU1P6iNpAwtRdh1DzixrKD72VbE3sKZyAyBSocQHleiHXxTM48Fbw%3D%3D)
