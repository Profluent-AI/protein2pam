# Protein2PAM

**Protein2PAM** is a deep learning framework to predict the PAM specificity of CRISPR systems from Cas proteins. 

Details about the models and their applications can be found in:  
**Nayfach, S., Bhatnagar, A., Novichkov, A., et al.** (2025). *Engineering of CRISPR-Cas PAM recognition using deep learning of vast evolutionary data. bioRxiv*. [https://doi.org/10.1101/2025.01.06.631536](https://doi.org/10.1101/2025.01.06.631536).

Protein2PAM is accessible via our webserver at: https://protein2pam.profluent.bio. It was developed at [Profluent](https://www.profluent.bio/) and code will be made available upon publication.

## Models

Below are the full listing of available models utilized in the manuscript and/or webserver:

| Model Name       | Input Protein/Domain | CRISPR Type     | Samples  | PAMs from Literature         | Used in Webserver?  |
|-------------------|---------------------|-----------------|----------|------------------------------|---------------------|
| `cas8`            | Cas8 or Cas10d      | Type I          | 28,410   |                              | ✅                  |
| `cas9`            | Cas9 PI-domain      | Type II         | 15,843   | [1-9](docs/REFERENCES.md)   | ✅                  |
| `cas12`           | Cas12 protein       | Type V          | 1,720    | [10-21](docs/REFERENCES.md)  | ✅                  |
| `cas9_full`       | Cas9 protein        | Type II         | 15,843   | [1-9](docs/REFERENCES.md)   | ❌                  |
| `cas9_full_nolit` | Cas9 protein        | Type II         | 15,731   |                              | ❌                  |
| `cas9_pid_nolit`  | Cas9 PI-domain      | Type II         | 15,731   |                              | ❌                  |
| `cas9_pid_nme`    | Cas9 PI-domain      | Type II         | 15,843   | [1-9](docs/REFERENCES.md)   | ❌                  |
| `cas12_no_lit`    | Cas12 protein       | Type V          | 1,675    |                              | ❌                  |


- `Model Name` should be specified if running Protein2PAM from python
- `Samples` indicates the number of protein:PAM pairs used for model training
- `PAMs from Literature` indicates that training samples were supplemented with *in vitro* determined PAMs from publications; for full listing, see [REFERENCES.md](docs/REFERENCES.md)
- `Used in Webserver?` indicates the models that are utilized by the [Protein2PAM Webserver](https://protein2pam.profluent.bio/)
- `cas9_pid_nme` model was trained using a training dataset in which Protein:PAM samples from Nme orthologs were upweighted

## Cite this work

If you use Protein2PAM in your research, please cite the following [preprint](https://doi.org/10.1101/2025.01.06.631536):
  
```bibtex
@article{nayfach2025protein2pam,
  title={Engineering of CRISPR-Cas PAM recognition using deep learning of vast evolutionary data},
  author={Stephen Nayfach and Aadyot Bhatnagar and Andrey Novichkov and Gabriella O. Estevam and Nahye Kim and Emily Hill and Jeffrey A. Ruffolo and Rachel Silverstein and Joseph Gallagher and Benjamin Kleinstiver and Alexander J. Meeske and Peter Cameron and Ali Madani},
  journal={bioRxiv},
  year={2025}
  publisher={Cold Spring Harbor Laboratory}
}
```
