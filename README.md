# Lab 5: Face Clustering using Hue and Saturation

---

## Aim
The aim of this lab is to:
- Detect faces from a group image using a face detection algorithm  
- Extract color-based features (Hue and Saturation) from detected faces  
- Cluster the faces into groups using a distance-based clustering method  
- Classify a given template face image into one of the formed clusters  

---

## Methodology

### 1. Face Detection
- The group image is first read and converted to grayscale.
- A Haar Cascade classifier is used to detect faces.
- Bounding boxes are drawn around all detected faces for visualization.

### 2. Feature Extraction
- The image is converted from **BGR to HSV** color space.
- From each detected face:
  - Mean **Hue** value is calculated
  - Mean **Saturation** value is calculated
- These values are used as feature vectors.

### 3. Clustering
- **K-Means clustering** with **two clusters** is applied.
- Faces are grouped based on their hue and saturation values.
- Centroids of each cluster are computed.

### 4. Template Classification
- The template image is processed in the same way.
- Hue and saturation features are extracted.
- The trained K-Means model predicts the cluster label.
- The template face is visualized along with the clustered faces.

---

## Visuals

### Face Detection on Group Image
![Group Face Detection](group_face_detection.png)

- Shows all detected faces in the group image.
- Each face is highlighted using a bounding box.
- Confirms correct face detection.

---

### Face Detection on Template Image
![Template Face Detection](template_face_detection.png)

- Shows face detection on the template image.
- Ensures the template face is correctly identified before clustering.

---

### Scatter Plot of Face Clusters
![Scatter Face Clusters](scatter_face_clusters.png)

- Scatter plot of faces using Hue (X-axis) and Saturation (Y-axis).
- Two clusters are clearly visible.
- Centroids of clusters are marked.

---

### Face Clustering using Image Markers
![Face Clustering Images](face_clustering_images.png)

- Each detected face is shown as a small image marker.
- Faces are positioned based on hue and saturation values.
- Helps visually understand clustering behavior.

---

### Template Face Clustering
![Template Face Clustering](template_face_clustering.png)

- Shows detected faces along with the template face.
- Template face is plotted in feature space.
- Demonstrates similarity with one of the clusters.

---

### Final Clustering with Template Image
![Final Face Clustering](final_face_clustering.png)

- Final result of clustering.
- Displays:
  - Cluster 0
  - Cluster 1
  - Centroids
  - Template face with predicted class label

---

## Result
- Faces from the group image were successfully detected.
- The detected faces were clustered into two groups using hue and saturation values.
- The template image was correctly classified into one of the clusters.
- The results show that simple color-based features can be used for basic face clustering.

---

## Tools and Libraries Used
- **Python** – Programming language  
- **OpenCV** – Face detection and image processing  
- **NumPy** – Numerical computations  
- **Matplotlib** – Plotting and visualization  
- **Scikit-learn** – K-Means clustering  

---

## Conclusion
This lab demonstrates a simple and effective approach to face clustering using color-based features. Hue and saturation values help group faces with similar color properties. The successful classification of the template image shows the usefulness of distance-based clustering methods for basic image analysis tasks.
