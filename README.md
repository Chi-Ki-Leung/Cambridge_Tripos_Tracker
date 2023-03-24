# CET Tripos Tracker
Developed and written by Chi Ki Leung

The tripos trackers on this repository are designed for the University of Cambridge's Chemical Engineering Tripos. The tripos trackers can help to summarise tripos practice progress, organise learning points, conduct efficient reviews and identify next steps. I benefited hugely from developing and using the tripos tracker for my revision and I hope they can be of some use to you too.

This documentation provides a user guide and technical details to the tripos trackers, which contain three main sections: dashboard, tripos notes and general comments. The CET IIA tripos tracker is used as an example.

Please note the example content in the user interfaces shown in this documentation are for demonstration purposes only. The example content do not bear any relevance to reality and should not be used as a reference.

## Dashboard
The dashboard summarises the number of tripos questions completed and to be done according to topics.

Column A lists the topics and groups them to relevant tripos papers according to the 2022-2023 Form and Conduct notices. Abbreviations are applied to the topics and they can be changed by editing the corresponding cell. For CET I, please delete as appropriate for the engineering/chemistry topic in paper 4. For CET IIA, the corrosion and materials topic is separated as two distinct topics of 'corrosion' (Corr) and 'materials' (Mat).

The 'Achievements' in column B summarises the number of tripos questions completed for each topic. The numbers are automatically updated according to the tripos question entries logged into the [tripos notes](#tripos-notes) section. The cells are automatically colour coded based on the relative numerical magnitude. A greater value will result in a lighter shade, as illustrated in the example user interface below.

In column C, the 'Ideal Ratio' between topics are the number of questions for each topic set in the tripos papers, according to the 2022-2023 Form and Conduct notices. The values for the ideal ratio can be changed, such as to account for personal strengths or weaknesses in different topics, by editing the relevant cells.

The 'target' in column D lists the number of questions that needs to be done for each topic in order to achieve the ideal ratio between topics set in column C. The cells are automatically colour coded based on the relative numerical magnitude. A greater value will result in a darker shade, as illustrated in the example user interface below. The [Algorithm for Target](#algorithm-for-target) section details how the target values are calculated.

### Algorithm for Target
For each topic, the ratio $R$ is calculated as follows

$$ R(\text{topic}) = \frac{\text{Achievement}(\text{topic})}{\text{Ideal Ratio}(\text{topic})} $$

The maximum $R$ among all topics, $R_{max}$, is then extracted.

If $R_{max} < 1$, the target $T$ for each topic is determined by

$$ T(\text{topic}) = \text{Ideal Ratio}(\text{topic}) - \text{Achievement}(\text{topic}) $$

If $R_{max} \ge 1$, the target $T$ for each topic is determined by

$$ T(\text{topic}) = R_{max} \times \text{Ideal Ratio}(\text{topic}) - \text{Achievement}(\text{topic}) $$

Lastly, irrespective of calculation methods, $T$ is rounded up to the nearest integer.

![Example_Dashboard](https://user-images.githubusercontent.com/121029649/227573392-66c81989-f707-4f0b-8e64-7aed68874aae.png)

## Tripos notes

This section is for logging completed tripos questions and reviewing learning points.

For each completed tripos question, insert the corresponding year, paper number and question number to the columns labelled Y (column A), P (column B) and Q (column C) respectively.

Next, insert the corresponding topic to column D. The value inserted to the topic column must match with one of the topics listed in column A of [dashboard](#dashboard), in order to successfully update the numerical value for achievements (column B of [dashboard](#dashboard)).

The subtopic should then be inserted to column E. The subtopic is designed for categorising tripos questions within the same topic for efficient review. For example, for the particle processing topic in CET IIA, the subtopics may include particle characterisation, cyclones and hoppers.

The possible input options for difficulty level (column F) are H (high), M (medium), L (low) and Outsy (out of syllabus). The cell will be automatically colour coded to red, yellow, blue and grey respectively upon entering the specific values. This is shown in the example user interface below. The Outsy option is designed for past tripos questions that no longer fall into the current syllabus.

For the remarks column (column G), learning points and comments from the tripos question shall be inserted. Press Alt+Enter to create new rows within the same cell to separate multiple comments, as shown in the example user interface below. These comments should ideally be specific to the topic/subtopic. General comments that are non-specific to the topic can be inserted in the [General comments](#general-comments) section.

The date when the tripos question is attempted should be inserted to column H.

The filter function is enabled for all columns A to H, so tripos questions can be easily selected for different review basis, such as by topic and/or by difficulty.

![Example_TriposNotes](https://user-images.githubusercontent.com/121029649/227582116-e94306bf-b3d4-4a22-a866-e6710fcc0c6f.png)

## General comments

Learning points and comments that are applicable to multiple or all topics can be inserted in this section. An example user interface is provided below.

![Example_GeneralComments](https://user-images.githubusercontent.com/121029649/227581063-f9b4ab09-4406-466a-9476-f248ecfa7924.png)
