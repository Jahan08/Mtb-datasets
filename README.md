Here we have raw and screened Mtb data with Bioactivity, collected fro m ChEMBL

# FOR Mtb ONLY, and Considering MIC as Bioactive property

## Data set
A dataset of inhibitors against Mtb (Target ID CHEMBL360) were compiled from the ChEMBL database that is comprised a total number of 88,284 compounds and 169144 bioactivity data points. The initial data set was assembled from several bioactivity measurement units including (in order of decreasing data
103 size) IC50, Ki, % activity, % inhibition, MIC, EC50, MIC etc. MIC was selected for further investigation as they constituted the largest subset with 25968 compounds. Only data points having nM as the bioactivity unit were selected for further study, which produced 12339 compounds (remove compounds with no SMILE data and no MIC value)
Furthermore, redundant compounds having different activity values were kept if the standard deviation of MIC was less than 2 and this resulted in 4329 compounds.

## Description of inhibitors 

Mtb inhibitors were encoded by a verctor of fingerprints descriptors accounting for its molecular constituents. Prior to calculating descriptors, salts were removed and tautomers were standardized using the built-in function of the PaDEL-Descriptor software.

Although fingerprint descriptors are able to capture the feature space of chemical compounds, however their ability to be used as descriptors for bioactivity modeling can vary. In fact, performance differences existing amongst the different fingerprint type has been the subject of several investigations into its utilization for bioactivity modeling. Riniker and Landrum (2013) benchmarked and assessed the performance of predictive models constructed from 2D fingerprint descriptors obtained from RDKit.

For this work we have considered 12 fingerprints:

|No             | FingerPrint                 | Number      | Description                                                                          | 
| ------------- | -------------               |-------------|--------------                                                                        |
|        1      |       CDK                   |  1024       |  Fingerprint of length 1024 and search depth of 8                                    |             
|        2      | CDK Extended                |  1024       |  Fingerprint of length 1024 bits describing ring features                            |
|        3      | CDK graph only|             |  1024       |  A special version that considers only the connectivity and not bond order           |          
|        4      |  E-State                    |  79         |  Electrotopological state atom types                                                 |             
|        5      |  MACCS                      |  166        |  Binary representation of chemical features defined by MACCS keys                    |             
|        6      |   PubChem                   |  881        |  Binary representation of substructures defined by PubChem                           |             
|        7      |  SubStructure               |  307        |  Presence of SMARTS patterns for functional groups                                   |             
|        8      | Substructure Count          |  307        |  Count of SMARTS patterns for functional groups                                      |             
|        9      | Klekota-Roth                |  4860       |  Presence of chemical substructures                                                  |             
|        10     | Klekota-Roth count          |  4860       |  Count of chemical substructures                                                     |             
|        11     | 2D atom Pairs               |  780        |  Presence of atom pairs at various topological distances                             |             
|        12     |  2D atomPairs count         |  780        |  Count of atom pairs at various topological distances                                |             
