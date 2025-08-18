# Optimizing Xenium In Situ data utility by quality assessment and best-practice analysis workflows

**Xenium** - 10X Genomics
- in situ sequencing-based (ISS)
- cell-identification algorithm begins with segmentation of DAPI-stained nuclei, followed by an expansion of the segmentation masks

Best practises
- **Cell pose** Identification of nuclei
- **Baysor** Assigning reads to individual cells
    - If cellular segmentation results in poor performance, segmentation-free methods such as SSAM9 or Points2Regions10 can be used to identify molecular signatures without identifying individual cells.
- Cell-by0gene matrix is generated after segmentation
- Cell type identification
    - Cell filetring
    - log-transformation and normalization
    - PCA
    - dimensionality reduction
    - clustering
- identifying spatially variable features (SVFs) is useful in distinguishing genes that explain the main spatial variation patterns within tissue
    - Hotspot least false positives
