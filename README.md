# Epidemic Spreading on Human Contact Networks – a MERS Case Study

Course project for *Life Data Epidemiology* (M.Sc. Physics of Data, University of Padova).

MERS outbreaks, such as those in Saudi Arabia and South Korea, were driven largely by transmission
inside hospitals. The project asks **which individuals in a contact network are the most effective
spreaders**, and whether their position in the network predicts the size of an outbreak.

## Approach

1. **Temporal network:** time-stamped face-to-face contacts, analysed as a sequence of snapshots.
2. **Network features per individual:** degree, PageRank and betweenness, and their fluctuations over
   time.
3. **SIR simulations** on the temporal network, seeded from each individual and from seeds selected by
   the features above, with the transmissibility set from a target basic reproduction number R₀.
4. **Comparison:** outbreak size and peak prevalence per seed, and their correlation with the seed's
   network features.

## Files and data

| File | Contents |
|---|---|
| `MERS.pdf` | Presentation: MERS background, network features, SIR results on a hospital-ward contact network (75 patients and staff, 4 days, 20-s resolution) |
| `new_mers_analysis.ipynb` | Network analysis and SIR simulations (python-igraph, networkx) |
| `MERS.ipynb` | First exploration of the contact data |

The notebooks run the same pipeline on the high-school contact network of Salathé *et al.* (PNAS 2010,
788 individuals), loaded from `school_salathe.csv`. The data files are not included.
