# Integrating 12 Spatial and Single Cell Technologies to Characterise Tumour Neighbourhoods and Cellular Interactions in three Skin Cancer Types
Prakrithi et al. 2025

## Typy karcinómov
* **Cutaneous squamous cell carcinoma (cSCC)**
* **Basal cell carcinoma (BCC)**
* **Melanoma**

### Pozadie
* **Keranocytové karcinómy**:
    * Basal cell carcinoma: 75-80%
    * cSCC: 20%

## Analýza expresie génov a bunková anotácia

### Diferenciálna expresia
* **Basal KCs** (KRT15+, KRT14+), 
* **Differentiating KCs** (PKP1+, KRT10+), 
* **Dysplastic KCs** (S100A8+, S100A9+), 
* **KC interferon** (IFI27+), 
* **KC cornified** (SBSN+, KRT2+, DSC1+) 
* **KC hair** (combination of KRT6B+, KRT17+, KRT16+, KRT5+)

### Anotácia
* **Level 1**: endothelial cells, fibroblasts, melanocytes, keratinocytes, immune cell types
* **Level 2**: immune cell types = B cell, Plasma, CD14+ Mono, DC, Langerhans cells (LC) , NK, Macrophages, T cells
* **Level 3**: DC = (DC1DC2), LC = (LC, Ki67+ LC), NK = (CD15+ NK, CD16- NK), Mac = (CD169+ Mac, CX3CR1+ Mac, INF+ Mac, TREM2+ Mac), T cell = (CD4+ Tcm, CD8+ Tem, NKT, Tref, CD8+ Tcm, CD8+ Tem)


### Identifikácia rakovinových buniek
* Integrating gene signatures and inferred copy number variation to identify cancer keratinocyte (KC) cells 
Cancer cell 
    * abnormal polyploidy based on CNV analysis 
    * high cancer module scores as calculated for genes that were upregulated in tumour compared to normal tissues
* **82,6%** klasifikovaných rakovinových buniek bolo medzi **dysplastickými KCs**, čo ich robí pravdepodobnými rakovinovými bunkami.

## Zmeny v bunkovom zložení
Overall shifts in cellular composition between non-cancer and cancer skin samples revealed by scRNAseq data
* **Fibroblast** proportions were consistently higher in melanoma and cSCC-BCC than in non-cancer tissue
* The increased presence of both the **lymphoid** (i.e. T, B and NK cells) and **myeloid** (i.e. monocytes, macrophages and dendritic cells) in malignant skin matched the elevated expression of immune gene signature depicted by the core gene suite analysis 
* the **basal** and **differentiating** KCs were more prominent in healthy skin, whereas dysplastic and IFN KCs were enriched in cSCC samples


## Porovnanie cSCC a melanómu

Comparison cSCC and melanoma
* **Enriched genes in cSCC compared to melanomas**: Myc targets, E2F pathways, G2M pathways, mTOR
    * PTCH2 upregulated in KC cancers signaling and DNA repair pathways
* **Enriched genes in melanocyte lesions compared to cSCC** : KRAS pathway, EMT pathway, IL-2/STAT5 pathway, and UV responses
    * SOX10 upregulated in melanoma

## Gény a signalizácia špecifická pre cSCC
* **The core cSCC genes**: enriched for immunological process GO terms
    * T-cell mediated cytotoxicity and antigen processing
* **Healthy signatures**: enriched for homeostatic processes
    * including "establishment of skin barrier" with genes like CLDN1, IL18, KLF4, KRT1, NFKBIZ, and TP63, suggesting potential loss of normal balance between proliferation and differentiation and skin integrity in cSCC.

* Distinct gene signatures differentiated cancer cSCC from normal KC at single cell resolution
    *  Enriched pathways: extracellular matrix (ECM) remodeling (MMP1, MMP3, MMP10, MMP12, MMP13, SERPINB3, SERPINB4, SERPINB13, SERPINE2)
    * Differentiation markers: SOX2, EOMES, DOK6, WNT5A.AS1, INHBA, S100A2, S100A7, S100A8, S100A9
    * Inflammatory/IL-17 pathway components (MMPs, S100s) → strong inflammatory signature


## Potvrdené signatúry rakovinových buniek cSCC
Confirmed cSCC cancer cell signatures by spatial multiomics
* **Consistently upregulated genes** across scRNAseq + Visium + CosMX + Xenium: SOX2, LAMP3, CXCL10, CXCL9, CCL5, UBE2C
    * **SOX2** → absent in normal epithelium; essential for cancer-initiating cells in cSCC
    * **CXCL10, CXCL9, CCL5** → tumor progression, T-cell infiltration, immune balance (upregulated in cSCC)
    * **LAMP3** → mature dendritic cells marker, antigen processing and T cell activation
    * **UBE2C** → cell cycle regulation, cell division

## Priestorové mapovanie (Spatial mapping) (GeoMX, Visium, CosMX)
* cSCC: high proportion of T cells (CD4+, CD8+, Treg) in immune regions
* Consistent spatial alignment between molecular signatures, histology, and spatial transcriptomics
* CosMX enables subcellular RNA localization (e.g., S100A8, KRT17 in KC cancer cells)



## Single-cell spatial heterogeneity analysis suggested a complex tumour community in melanomas
*  **Rao’s quadratic entropy score** - sum of the pairwise distances between all cell types, weighted by their relative abundances.
    * measure of spatial heterogeneity that considers both the abundance of different cell types and the dissimilarity between them
    * $$ Q = \sum^S_{i=1} \sum^S_{j=1} d_{ij} p_i p_j $$
        * S is the total number of cell types in the region of interest.
        * p_i and p_j are the relative abundances (proportions) of cell types i and j.
        * d_ij is the distance or dissimilarity between cell types i and j
* Trend that melanomas do not adhere to each other as much as KC cancer cells, and so their neighbour cells can be more diverse (page 8)


## Single-cell predictions of CCI suggest differential interactions in healthy and cSCC cancer patients 
* CellChat - cell to cell interactions for the scRNAseq cSCC dataset
* Cancer specific core LR pairs were enriched for immune-related functions 
    * MHC class II complex assembly

## Spatial transcriptomics enhances the accuracy and specificity of LR interaction predictions by incorporating spatial constraints 
* spatially-constrained two-level permutation (SCTP) in **stLearn** software to predict spatially-informed LR interactions.
    * detected false positives (XCL1-XCR1) and missed interactions (CXCL12-CXCR4, CCL9-CCR7) (Fig S19ab)

## Different ligand-receptor interactions specific for a cancer type show important roles of angiogenesis, integrins, and fibroblast growth factors
* Aplication of multi-platform, multi-sample
cell cell interaction analysis (MMCCI) approach
* Detected LR pair enrichments:
    * BCC:
        * stromal remodeling, especially angiogenesis: 
            * Interleukins: IL6-IL6R, IL6-IL6ST, IL1B-IL1RN-IL1R2
            * Chemokines: CXCL2-CXCR1, CCL2-ACKR4 
            * Fibronectins: FN1-ITGB8, FN1-ITGB6
        * Canonical WNT signaling pathways (WNT5A-FZD7, WNT5A-FZD8), supported by EPCAM-EPCAM interactions
        * WNT pathway coordinates with Hedgehog (HH) signaling to maintain BCC cell proliferation and sustain cancer stem-like cells
    * cSCC:
        * Osteopontin (SPP1) interactions, uniquely expressed in cSCC:
            * SPP1-ITGB1 and SPP1-ITGAV
            * SPP1-CD44 and SPP1-ITGB5 (upregulated vs BCC and melanoma)
        * SPP1 interacting with integrins and CD44 may activate intracellular signaling pathways:
            * PI3K/Akt, MAPK/ERK, and FAK — promoting cell survival, proliferation, and growth
        * Additional signaling activations by FLT1 and CSF3-CSF3R interactions
        * Angiogenesis-related LR pairs upregulated: CD38-PECAM, VEGFB-FLT1 (VEGFR-1), CXCL1-CXCR2
        * Inflammation promoted by calprotectin (S100A8, S100A9) interacting with TLR4 on immune cells
        * Angiogenesis is elevated in both BCC and cSCC but regulated through distinct pathways
    * Melanoma:
        * Strong enrichment of collagen interactions (15/37 LR pairs specific to melanoma):
            * COL1A1, COL1A2, COL3A1 interacting with integrin receptors (ITGA, ITGB)
            * Notable pairs: COL1A1-ITGA2, COL1A1-ITGB1, COL1A1-ITGA5, COL1A2-ITGA2, COL1A2-ITGB1
        * Collagen-integrin interactions contribute to:
            * Microenvironment remodeling, pro-tumorigenic and immunosuppressive niches
            * Promotion of angiogenesis
            * Activation of MEK/ERK signaling pathway
        * Four collagen-interaction genes involved in DNA damage response (DDR1, DDR2)
        * Fibroblast Growth Factor (FGF) interactions (6/37 pairs):
            * FGF1-CD44, FGF2-CD44, FGF2-FGFR1, FGF18-FGFR1, FGF1-FGFR1, FGF9-FGFR1
        * FGF signaling enhances melanoma proliferation via MAPK/ERK, PI3K/AKT, and JAK/STAT pathways
        * Some FGF pathways are therapeutic targets in melanoma (e.g., FGF2/FGFR signaling)

## Different interactions between cell-cell pairs highlight the roles of fibroblast, T cells and melanocytes/keratinocytes 
* Methods:
    * Used interaction network graph analysis combining multiple replicates
    * Statistical comparison of interacting cell types performed using MMCCI (multiplatform, multimodal cell-cell interaction analysis)
    * Interaction strength defined as cumulative p-value from all samples for each interaction
* Cell type level findings:
    * cSCC and BCC show more similarity to each other than to melanoma (Fig S20a)
    * Most common interactions across all three cancers: fibroblasts interacting with immune cells and keratinocytes (KC) (Fig S20a)
    * Stronger fibroblast → T cell interactions in cSCC and BCC vs melanoma
    * Higher fibroblast → melanocyte interaction in melanoma (Fig 6b)
    * More fibroblast → KC cell interactions in cSCC and BCC, especially with differentiating keratinocytes (Fig 6b)

* Ligand-Receptor (LR) pair level findings:
    * Cancer type-specific LR pairs enriched in key cancer-related pathways such as EMT (Fig S20d)
    * MIF-CD44 identified as one of the top two LR pairs differing most between cancer types (Fig S20b)
        * Strong interactions between macrophages and KC cells, fibroblasts, and T cells (Fig S20c)
    * CD80-CTLA4 was the most active differentially interacting LR pair (Fig S20d)
        * In melanoma, key cell-cell pairs for CD80-CTLA4: fibroblast-melanocyte and fibroblast-T cell (Fig S20e)
    * Top LR pairs associated with T cells and melanocytes summarized (Fig S20f)

* Implications:
    * LR interactions highlight roles of CD44, extracellular matrix, and immune system
    * Provide insight into potential drug targets for melanoma at a systematic level (Fig 6d)

## Integrative confirmation of LR signalling at RNA level reveals enrichment of IL34-related antigen-presenting pathways in melanoma

* Global LR interaction analysis:
    * Over 2000 known LR pairs analyzed across spatial modalities
    * IL34-CSF1R identified as a top interacting pair, with higher levels in melanoma vs cSCC and BCC (Fig 6a)
* Biological background:
    * IL34: cytokine mainly produced by keratinocytes
    * CSF1R: receptor activating immune cells, especially macrophages and Langerhans cells
    * High IL34 expression linked to poor survival in lung cancer due to CSF1R-mediated activation of tumor-associated macrophages (Baghdadi et al., 2016, 2018)
    * IL34-CSF1R interaction in melanoma associated with drug resistance (Giricz et al., 2018)
* Validation and spatial localization:
    * RNAScope analysis confirmed co-localization of IL34 and CSF1R (Fig S21)
    * Strongest interaction in melanoma, but also detected in BCC and cSCC dermis at immune-rich regions using STRISH pipeline (Fig 7b)
    * Consistent with spatial single-cell gene expression data (Fig 6c)
    * Both genes detected in healthy and cSCC scRNA-Seq atlas
    * Visium (low spatial resolution) shows IL34-CSF1R colocalization in dermis (Fig 7a)
    * Single-cell spatial data (STOmics, Curio-Seeker melanoma samples) show spatial proximity of IL34 and CSF1R expressing cells (Fig 7b)
* Functional enrichment analyses:
    * Visium spot comparisons (interacting vs non-interacting) show enrichment in:
        * Antigen processing pathways (Fig 7c)
        * Lipid metabolism pathways (Fig 7d)
    * Upregulated genes in IL34-CSF1R positive spots:
        * Melanoma: 531 genes, with GO enrichment for immune and lipid-related functions
        * BCC: 758 genes, no GO enrichment found
    * Suggests important roles for IL34-CSF1R upregulation in melanoma immune and metabolic functions

## Integrating spatial analysis with genetic association of cancer traits from population-scale data
* Objective:
    * Integrate spatial omics data with GWAS summary statistics to map skin cancer risk SNPs to spatial cell types and domains
    * Applied gsMAP method to map genetic association signals (SNP effect sizes) for cSCC, BCC, and melanoma heritability to specific cell types/spatial regions
* Mapping approach:
    * Identify gene markers specifically and highly expressed in cell types or spatial domains using spatial transcriptomics data
    * Map SNPs to these genes based on linkage disequilibrium (LD) distance
    * Test significance of cumulative SNP effects (Cauchy P value) vs SNPs not associated with marker genes (Song et al., 2024)
* Analysis details:
    * Calculated Gene Specificity Scores (GSS) for genes highly expressed in spatial neighborhoods
    * Mapped SNPs to genes within GSS based on transcription start site proximity
    * Computed proportion of trait heritability captured by SNPs linked to GSS genes per spot/cell via stratified LD score regression
    * Aggregated P values of spots/cells within spatial regions or cell types to assess significance
* Key findings from Visium data:
    * Genetic association signals for BCC, cSCC, and melanoma enriched in epidermis
    * Signals often spatially localized, not uniformly distributed across outer skin layer (Fig 8a)
    * Top cell type associations:
        * Melanoma: melanocytes and differentiating keratinocytes (KC)
        * Fibroblasts showed strong associations across all three cancers (melanoma, cSCC, BCC) (Fig 8b)
    * cSCC and BCC associate strongly with dysplastic KC (more cSCC), KC hair (more BCC), and KC cornified (both, higher than melanoma) (Fig 8b)
* Single-cell resolution mapping (CosMX data):
    * Tumor regions show strongest spatial heritability explained by SNPs linked to GSS genes (Fig 8c)
    * Followed by immune regions; stroma showed lowest spatial heritability
* Ligand-Receptor (LR) gene correlations:
    * Identified LR pairs with significant correlation between spatial gene specificity scores and genetic association P values
    * Highlights how genetic signals may influence cell-cell interactions in spatial microenvironment
    * Strong interactions found between:
        * KC dysplastic (cSCC) and KC hair (BCC)
        * More immune interactions in melanoma, especially T cell related (Fig 8d)
    * Genetic association visualization between T cells and melanoma via LR pairs: IL34-CSF1R and LTB-LTBR
        * Strongest association for LTB-LTBR at epidermis-dermis junction; IL34-CSF1R less spatially specific (Fig 8e)
* Genome-wide associations and spatial expression:
    * Top genes with highest correlation to melanoma spatial specificity include MITF, TYR, MX2
    * CSF1R, LTB, and LTBR among top 50 correlated genes for melanoma spatial expression (Fig 8f)
    * Genome-wide significant SNPs linked to T cell and melanoma marker genes show strongest Manhattan plot signals
    * Suggests melanoma heritability is strongly influenced by effects on T cells and melanocytes