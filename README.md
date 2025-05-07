# publication_process Metadata Schema for scholarly publications

Scholarly publications are very well described by standardized metadata.
Existing frameworks focus on 

- bibliographic description
- legal aspects including access rights
- technical metadata like size of files etc.

However, up to now - at least to our knowledge - there exists no metadata
schema to describe the process through which the publication was created, including peer review, reviewers, communication between publisher and author.

Through the [Langzeitverfügbarkeit Bayern](https://lzv-bayern.de/) project we tried to tackle this task as a way to structure publication data for long time archiving.

The origin of the metadata were several online Open Access journals hosted by the University Library Regensburg, using the open source software [OJS](https://pkp.sfu.ca/software/ojs/).

## Metadata Schema: Overview

- 






## Data schema for individual articles

The overall tree structure looks like this:
```
publication [1]
    |
    |--- article_source [2]
    |    |
    |    |--- dc:title [2.1]
    |    |--- dc:creator
    |    |--- dc:...
    |
    |--- manuscript [3]
    |    |
    |    |--- dc:creator [3.1]
    |    |--- dc:date
    |    |--- dc:...
    |
    |--- peer_review [4]
    |    |
    |    |--- reviewed_manuscript [4.1]
    |    |    |
    |    |    |--- dc:creator [4.1.1]
    |    |    |--- dc:date
    |    |    |--- dc:...
    |    |
    |    |--- decision [4.2]
    |    |    |
    |    |    |--- dc:creator [4.2.1]
    |    |    |--- dc:date
    |    |    |--- dc:...
    |    |
    |    |--- revised_manuscript [4.3]
    |    |    |
    |    |    |--- dc:creator [4.3.1]
    |    |    |--- dc:date
    |    |    |--- dc:...
    |    |
    |    |--- comment [4.4]
    |         |
    |         |--- dc:creator [4.4.1]
    |         |--- dc:date
    |         |--- dc:...
    |    
    |
    |--- publication_proof [5]
    |    |
    |    |--- dc:creator [5.1]
    |    |--- dc:date
    |    |--- dc:...


```


| No.   | Field name            | Values                                                                                                                                             | Data Type | Repeatable | Required | Description/Remarks |
|:------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|:----------|:-----------|:---------|:--------------------|
| 1     | `publication`         |                                                                                                                                                    |           | No         | Yes      | Wrapper for the Publication Process. |
| 2     | `article_source`      |                                                                                                                                                    |           | No         | Yes      |  |
| 2.1   | `dc:...`              |[This is a placeholder for Dublin Core Elements 1.1, please refer to the corresponding definitions and comments.](http://purl.org/dc/elements/1.1/) | String    | Yes        | No       |  |
| 3     | `manuscript`          |                                                                                                                                                    |           | Yes        | No       |  |
| 3.1   | `dc:...`              |[This is a placeholder for Dublin Core Elements 1.1, please refer to the corresponding definitions and comments.](http://purl.org/dc/elements/1.1/) | String    | Yes        | No       |  |
| 4     | `peer_review`         |                                                                                                                                                    |           | Yes        | No       |  |
| 4.1   | `reviewed_manuscript` |                                                                                                                                                    |           | Yes        | No       |  |
| 4.1.1 | `dc:...`              |[This is a placeholder for Dublin Core Elements 1.1, please refer to the corresponding definitions and comments.](http://purl.org/dc/elements/1.1/) | String    | Yes        | No       |  |
| 4.2   | `decision`            |                                                                                                                                                    |           | Yes        | No       |  |
| 4.2.1 | `dc:...`              |[This is a placeholder for Dublin Core Elements 1.1, please refer to the corresponding definitions and comments.](http://purl.org/dc/elements/1.1/) | String    | Yes        | No       |  |
| 4.3   | `revised_manuscript`  |                                                                                                                                                    |           | Yes        | No       |  |
| 4.3.1 | `dc:...`              |[This is a placeholder for Dublin Core Elements 1.1, please refer to the corresponding definitions and comments.](http://purl.org/dc/elements/1.1/) | String    | Yes        | No       |  |
| 4.4   | `comment`             |                                                                                                                                                    |           | Yes        | No       |  |
| 4.4.1 | `dc:...`              |[This is a placeholder for Dublin Core Elements 1.1, please refer to the corresponding definitions and comments.](http://purl.org/dc/elements/1.1/) | String    | Yes        | No       |  |
| 5     | `publication_proof`   |                                                                                                                                                    |           | Yes        | No       |  |
| 5.1   | `dc:...`              |[This is a placeholder for Dublin Core Elements 1.1, please refer to the corresponding definitions and comments.](http://purl.org/dc/elements/1.1/) | String    | Yes        | No       |  |

