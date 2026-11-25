# Data Analysis and Machine Learning: Assignment 1

# a) Dataset
This dataset contains 22 launch photographs of space shuttles during ascent, taken from NASA's Kennedy Space Center Media Archive and accessed through the Internet Archive. Each item is one photograph showing a visible space shuttle ascending.

# b) Motivation
I created this dataset to examine how space shuttle launches are visually documented. My dataset could help in answering research questions about which missions and space shuttles are more commonly photographed by NASA and how viewpoints and visual framing differ between photographs of the same launch.

# c) Selection Criteria
I included photographs in which the space shuttle has visibly lifted from the launch pad and is ascending; I excluded drawings, simulations, renderings, and photographs showing only smoke from the launch. Multiple photographs of the same launch were permitted when they showed different viewpoints and framing. The selected photographs cover a publication year range of 1983–2007 and depict the space shuttles Endeavour, Atlantis, Discovery, and Columbia; other publication periods and space shuttles are not represented in this dataset.

# d) Data Collection Process
I manually selected and downloaded the photographs from NASA's Kennedy Space Center Media Archive on the Internet Archive, and I recorded their metadata from their Internet Archive item pages on 24 November 2026. The 'source' column links to these pages, whereas the 'original_source' column links to the original source URLs supplied in the archive records, the latter of which were not working when checked on 24 November 2026.

# f) Structure
My folder structure is as follows:
```
├── data                   # Original photograph files of NASA space shuttle launches
├── .gitignore             # Ignored files
├── README.md              # Dataset documentation
├── check_dataset.ipynb    # Pandas checks and basic summaries
├── metadata.csv           # One metadata row per launch photograph
└── requirements.txt       # Required Python packages
```

My codebook is as follows:

| Variable | Description | Type | Allowed values / missing values |
|---|---|---|---|
| id | Unique photograph identifier recorded on the Internet Archive | String (identifier) | Letters, numbers, hyphens; not permitted |
| file | Relative path to the downloaded photograph | String (file path) | `data/<shortened id>.<file format>`; not permitted |
| source | Internet Archive item page where the photograph was accessed | String (URL) | Full URL; not permitted |
| original_source | Original source URL recorded on the Internet Archive | String (URL) | Full URL; empty if unknown |
| licence | Copyright status or reuse terms | String | NASA's reuse rules; empty if unknown |
| mission | Mission recorded in the description of each photograph on the Internet Archive | String (categorical) | Mission codes; empty if unknown |
| space_shuttle_name | Name of the NASA space shuttle depicted in each photograph | String (categorical) | Space shuttle name; empty if unknown |
| date_published | Publication date recorded on the Internet Archive | Integer (date) | YYYY-MM-DD; empty if unknown |
| publisher | Publisher named on the Internet Archive | String | Publisher name; empty if unknown |

# g) Uses and Limitations
This dataset can be used for visual and descriptive comparisons of the selected missions or space shuttles, and for a visual examination of NASA's launch photography from 1983–2007. The small, non-random selection and repeated coverage of certain launches mean that it should not be used as a representation of all NASA launches or launch photographs, nor should it be used to infer launch frequency or safety.

# h) Ethical and Legal Aspects
According to NASA's Media Usage Guidelines, NASA's photographs are not subjected to copyright and may be used for educational and informational purposes; NASA should be acknowledged as the source of the material. The source's license is Public Domain Mark 1.0. This data does not contain personal information, and I am permitted to share it.

# i) Licence and Citation
My original documentation and any copyrightable contributions to the metadata and dataset selection are licensed under CC BY 4.0. This licence does not apply to the source photographs, which remain subject to NASA's Media Usage Guidelines, and any item-specific rights information recorded in the metadata.  
Curtis, B. L. (2026). *Launch photographs of NASA space shuttles* (Version V1) [Dataset]. GitHub. https://github.com/Betholith/daml-assignment1.
