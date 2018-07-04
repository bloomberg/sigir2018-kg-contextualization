# sigir2018-kg-contextualization

This repository contains the data with manual annotations gathered using CrowdFlower for our SIGIR 2018 paper:

> Nikos Voskarides, Edgar Meij, Ridho Reinanda, Abhinav Khaitan, Miles Osborne, Giorgio Stefanoni, Kambadur Prabhanjan and Maarten de Rijke: Weakly-supervised Contextualization of Knowledge Graph Facts. 2018. In Proceedings of the 41st International ACM SIGIR conference on Research and Development in Information Retrieval (SIGIR '18).

We provide more details on this dataset at https://www.techatbloomberg.com/research-weakly-supervised-contextualization-knowledge-graph-facts/. 

The [file](sigir2018-kg-contextualization.gz) itself is gzipped and structured as follows.

```json
{
    "query_id" : {
        "relation": "", // the predicates of the query relation
        "query": "", // query fact path
        "candidates": [ // list of candidate facts
        	{
	            "cand_id": { // candidate fact id
                    "cf_label": 0, // relevance label from CrowdFlower annotations
                    "dist_sup_label": 0, // relevance from distant supervision
    	            "path": [], // the candidate fact path
                }
            }
        ]
    }
}
```

Note that the format of the paths is as follows:

```json
 ([subject_id, list_of_subject_types], pred, [object_id, list_of_object_types])
```

