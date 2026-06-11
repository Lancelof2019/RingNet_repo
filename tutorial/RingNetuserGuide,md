# RingNet Network Viewer Tutorial

Welcome to the **RingNet Network Viewer**! This guide provides a comprehensive overview of the interface controls and recommended workflows for visualizing complex multi-omics networks.

---

## Quick Overview
The RingNet interface is designed for high-dimensional biological data visualization, supporting:

- **Network Analysis:** Selection, layout adjustment, and node search.
- **Multi-omics Integration:** Color control for multiple data layers (Data1-Data4).
- **Discovery Tools:** Pattern Discovery, Similarity/Difference displaying.
- **Data Export:** Snapshot saving and high-quality image export (PNG/SVG).

---

## 1. Network & Layout Controls

### Network Selection
Select the specific network or community you wish to explore. Note that **only one network** is displayed at a time to maintain clarity.

### Layout Adjustment
Arrange nodes on the canvas using various algorithms. Changing the layout **only affects node positions** and does not modify the underlying data.

| Layout Type | Best Use Case |
| :--- | :--- |
| **Loose Balanced / Soft Spread** | General network exploration |
| **Spread Force** | Highlighting clusters |
| **Component Grid** | Separating disconnected components |
| **Concentric / Circle** | Hierarchical or symmetric structures |
| **Grid** | Uniform distribution |

### Degree Range Filter
Filter nodes based on their connectivity.
> **Example:** Setting `Degree Range: 0 – 500` will only show nodes whose visible degree falls within this specific range.

---

## 2. Export & Snapshot Management

Keep your work safe and ready for publication with these tools:

- **Fit:** Instantly fit the entire graph into the visible canvas.
- **Save PNG:** Export the current view as a standard image.
- **Save SVG:** Export as an editable vector image (Recommended for **publications**).
- **Save JSON:** Export the raw network data in JSON format.
- **Save Snapshot:** **Highly Recommended.** Saves the *entire* visualization state, including:
  - Node positions, colors, and filters.
  - Pattern Discovery and Similarity/Difference settings.
  - Highlighted nodes/edges and search states.

---

## 3. Node Search & Interaction

- **Node Search:** Search for specific genes or node names. The matched node and its immediate neighbors will be highlighted, while others are dimmed.
- **Clear:** Removes search highlights. If **Pattern Discovery** is active, clearing the search returns you to the pattern state rather than resetting the entire graph.

---

## 4. Multi-omics Node Colors

Nodes are visualized with concentric rings representing different data types:

| Layer | Common Biological Meaning |
| :--- | :--- |
| **Data1** | Gene Expression |
| **Data2** | Methylation |
| **Data3** | CNV (Copy Number Variation) |
| **Data4** | SNV / Mutation Data |
| **Group** | Stage, Grade, or Class labels |

> **Customization:** Each layer supports a three-color gradient: 
> `[ Negative Color ]` — `[ Neutral Color ]` — `[ Positive Color ]`

---

## 5. Data Filtering & Normalization

Refine your view by selecting specific data layers and scales:

1. **Select Layer:** Choose between Data1, Data2, Data3, or Data4.
2. **Choose Scale:** 
   - `Raw`: Original values.
   - `Min-Max Norm`: Scaled between 0 and 1.
   - `Z-score`: Standardized relative to the mean.
3. **Value Range:** Use the slider to filter nodes based on the selected scale.

---

## 6. Pattern Discovery

Identify **anti-correlated** multi-omics patterns (e.g., High Expression + Low Methylation).

### How it works:
Pattern Discovery typically compares **Data1** and **Data2** using Z-score thresholds:
- **Data1 High/Low:** Define thresholds for high/low states.
- **Data2 High/Low:** Define thresholds for high/low states.
- **Highlighting:** Nodes matching opposite directions (High/Low or Low/High) are automatically highlighted.

---

## 7. Analysis Modes (Group-aware vs. Group-free)

Depending on whether you have stage or group information, the viewer adjusts its metrics:

### **Group-aware Mode** (With Stage Data)
- **TrendScore:** Measures if the pattern follows a group-level trend.
- **GroupScore:** Measures the strength of group-aware evidence.
- *Best for: Stage, Class, or Condition analysis.*

### **Group-free Mode** (No Stage Data)
- **GlobalPatternRate:** Measures how many samples support the pattern globally.
- **GroupScore:** Measures global evidence without using labels.

---

## 8. Sample Selection (Similarity & Difference)

These functions change **which sample slices** are shown in the node rings without deleting any data.

- **Difference Displaying:** Selects samples with the most multi-omics variation.
- **Similarity Displaying:** Selects samples that are most coherent.
- **Samples per Group:** Controls the number of selected samples (Default: `8`).

---

## 9. Edge Controls

Fine-tune the connections between nodes:

- **Edge Colors:** Map weights to a color gradient (Negative/Neutral/Positive).
- **Show Weights:** Toggle numeric labels on edges.
- **Edge Data Norm:** Choose between `Raw`, `Min-Max`, or `Z-score`.
- **Color by `interact_id`:** Color edges by interaction type instead of weight.

---

## 10. Viewer Types

| Directed Viewer | Undirected Viewer |
| :--- | :--- |
| Preserves edge direction (`A → B` ≠ `B → A`). | Ignores direction (`A → B` & `B → A` are merged). |
| Best for: Regulatory or Signaling networks. | Best for: Similarity or Co-expression networks. |

---

## 11. Recommended Workflow

1.  **Initialize:** Select your **Network** and choose a **Layout**.
2.  **Style:** Adjust **Node Colors** and **Edge Colors** for clarity.
3.  **Filter:** Apply **Node/Edge Filters** to remove noise.
4.  **Discover:** Use **Pattern Discovery** to find biological insights.
5.  **Refine:** Use **Difference/Similarity** displaying to focus on key samples.
6.  **Locate:** Use **Node Search** to find specific genes of interest.
7.  **Export:** Save a **Snapshot** for future work and export **SVG** for your paper.

---

## Notes
- **Non-Destructive:** Layout and filtering changes do not modify the original data.
- **Snapshots:** Always save a snapshot before closing to preserve your customized view.
