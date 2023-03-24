# CET Tripos Tracker
Developed and written by Chi Ki Leung

The tripos trackers on this repository are designed for the University of Cambridge's Chemical Engineering Tripos. The tripos trackers can help to summarise tripos practice progress, organise learning points, review efficiently and identify next steps. I benefited hugely from developing and using the tripos tracker for my revision and I hope they can be of some use to you too.

This documentation provides a user guide and technical details to the tripos trackers, according to their three main sections: dashboard, tripos notes and general comments. The CET IIA tripos tracker is used as an example.

## Dashboard
The dashboard summarises the number of tripos questions completed and to be done according to topics.

Column A lists the topics and groups them to relevant tripos papers according to the 2022-2023 Form and Conduct notices. Abbreviations are applied to the topics for convenience and they can be changed by editing the corresponding cell. For CET I, please delete as appropriate for the engineering/chemistry topic in paper 4. For CET IIA, the corrosion and materials topic is separated as two distinct topics of 'corrosion' (Corr) and 'materials' (Mat).

The 'Achievements' in column B summarises the number of tripos questions completed for each topic. The numbers are automatically updated according to the tripos question entries logged into the [tripos notes](#tripos-notes) section. The cells are automatically colour coded based on the relative magnitude of the numbers. A greater value will result in a lighter shade, as illustrated in the example user interface below.

The 'Ideal Ratio' between topics in column C are the number of questions for each topic set in the tripos papers, according to the 2022-2023 Form and Conduct notices. The values for the ideal ratio can be changed, such as to account for personal strengths or weaknesses in different topics, by editing the relevant cells.

The 'target' in column D lists the number of questions that needs to be done for each topic in order to achieve the ideal ratio between topics set in column C. The cells are automatically colour coded based on the relative magnitude of the numbers. A greater value will result in a darker shade, as illustrated in the example user interface below. The [Algorithm for Target](#algorithm-for-target) section details how the target values are calculated.

### Algorithm for Target
For each topic, the following ratio $R$ is calculated as follows

$$ R(\text{topic}) = \frac{\text{Achievement}(\text{topic})}{\text{Ideal Ratio}(\text{topic})} $$

The maximum $R$ among all topics, $R_{max}$, is then extracted.

If $R_{max} < 1$, the target $T$ for each topic is determined by

$$ T(\text{topic}) = \text{Ideal Ratio}(\text{topic}) - \text{Achievement}(\text{topic}) $$

If $R_{max} \ge 1$, the target $T$ for each topic is determined by

$$ T(\text{topic}) = R_{max} \times \text{Ideal Ratio}(\text{topic}) - \text{Achievement}(\text{topic}) $$

Lastly, irrespective of the method used to determine $T$, $T$ is rounded up to the nearest integer.

## Tripos notes


## General comments
