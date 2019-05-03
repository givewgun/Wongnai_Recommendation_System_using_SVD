Wongnai_Recommendation_System_using_SVD

Author: Gun Kaewngarm, Non Kositkittiwanit

How to run the model?

*****This model use data from wongnai database of project 2. You must have the database set up in your system (locally)*****

Run the jupyter notebook files in order
1.	User_res_rating_normalizing.ipynb
	a.	This file will query and process the user-restaurant rating from database and generate file user_res_rating_df.csv.
2.	rank_score_normalized.ipynb 
	a.	This will generate res_rank_score_dict.npy (The rank_score data) to be used in other notebook.
3.	Teop_res_gen.ipynb
	a.	Preparing data
	b.	This will generate train_data_matrix.npz, factor_mean_data_matrix.npz, res_dict.npy and user_dict.npy to be used in model
4.	svd-2.ipynb
	a.	This will run model and recommend restaurant to non-new user
	b.	Will generate a predict_raw.txt file
5.	user_region.ipynb
	a.	This will query and process the user’s location(provinces)
	b.	Will generate user_region_dict.npy and user_c_region_dict.npy
6.	restaurant_region.ipynb
	a.	This will query and process the restaurant’s location(provinces)
	b.	Will generate res_region_dict.npy
7.	fill_missing_per_region.ipynb
	a.	This file will fill the recommendation for new user
	b.	This will fill the predict_raw.txt file and output the final answer file
