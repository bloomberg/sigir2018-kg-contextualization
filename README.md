# sigir2018-kg-contextualization

This repository contains the data with manual annotations gathered using CrowdFlower for our SIGIR 2018 paper:

> Nikos Voskarides, Edgar Meij, Ridho Reinanda, Abhinav Khaitan, Miles Osborne, Giorgio Stefanoni, Kambadur Prabhanjan and Maarten de Rijke: Weakly-supervised Contextualization of Knowledge Graph Facts. 2018. In Proceedings of the 41st International ACM SIGIR conference on Research and Development in Information Retrieval (SIGIR '18).

We provide more details on this dataset at https://www.techatbloomberg.com/research-weakly-supervised-contextualization-knowledge-graph-facts/. 

The [file](sigir2018-kg-contextualization.gz) itself is gzipped and has the following fields.

Field | Description
--- | ---
`relation` | The predicates of the query relation
`query` | The query fact path
`candidates` | The list of candidate facts
`cand_id` | The candidate fact ID
`cf_label` | The relevance label from CrowdFlower annotations
`dist_sup_label` | The relevance label from distant supervision
`path` | The candidate fact path: `([subject_id, list_of_subject_types], pred, [object_id, list_of_object_types])`

Note that the format of each path is as follows.

Field | Description
--- | ---
`subject_id` | The subject ID
`subject_type_1...n` | The types of the subject
`predicate` | The predicate
`object_id` | The object ID
`object_type_1...n` | The types of the object

I.e., 
```json
{
    "query_id" : {
        "relation": "",
        "query": "",
        "candidates": [
            {
                "cand_id": {
                    "cf_label": 0,
                    "dist_sup_label": 0,
                    "path": []
                }
            }
        ]
    }
}
```