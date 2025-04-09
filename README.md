# SGRD and SG2
With the rapid development in the field of artificial intelligence, isolated object-level perception tasks have achieved tremendous success. However, in the field of object group understanding, existing remote sensing scene graph generation (SGG) methods, a structured description of objects and their inter relationships, tend to focus on comprehensive scenes with numerous elements and complex relationships, which may obscure the characterization of high-value relationships. Consequently, in specific scenes, the concise and efficient description of spatial-temporal relationships between high-value objects (such as vehicles and ships) presents a challenge.

Simultaneously, the complexity of spatial relationships within the remote sensing object group necessitates the use of global context to aid in predicting these relationships, while fine-grained local context is essential for accurate relationship prediction. To address this, we propose a Ship Group Relationship Description method (SGRD) based on remote sensing SGG with a global and local context fusion network, called GLFN. The proposed network integrates global feature fusion through a Transformer-based self-attention mechanism and enhances local feature fusion using a graph convolutional network focused on object-specific graph structures. Additionally, we introduce a new dataset featuring Ship Group Scene Graphs, named SG2, derived and refined from the HRSC2016 dataset. Experimental results demonstrate that GLFN achieves competitive performance on SG2 in specific scenes compared to classical and recent SGG methods, offering potential for relationship-guided change detection and situational awareness.

# Datasets
Due to the directional and dense nature of objects in remote sensing images, the horizontal bounding boxes used in the above datasets tend to include background or other object information, causing significant interference in accurately extracting object features. This interference, in turn, severely impacts the accuracy of scene graph generation. To address the lack of scene graph datasets focused on spatial relationships within object groups in specific scenarios, this paper constructs the Ship Group Scene Graph Dataset (SG2) based on the HRSC2016 dataset. To balance scene graph precision and accuracy in specific applications and facilitate simple and efficient remote sensing image understanding, this paper defines 10 spatial relationship categories: side-by-side, end-to-end, and eight orientation relationships (up, down, left, right, upper-left, upper-right, lower-left, and lower-right). The specific construction principles are illustrated in Fig.data1.

The ship object labels in the HRSC2016 dataset were used as the foundation, while image data containing only a single ship were discarded (as they cannot reflect any relationships within a ship group). Spatial relationship annotations were performed semi-automatically, following the triplet format of <subject, relationship, object>. The dataset was split into training, testing, and validation sets, with 70\% allocated for training, 20\% for testing, and 10\% for validation. Fig.data2 provides examples of labeled data in the SG2 dataset.

# Code and Dataset are coming soon.
