https://stackoverflow.com/a/64016190/6615163

for index, row in final_frame.iterrows():
    if row['monthly_engagement_score_x'] == 0:
        final_frame.at[index, 'monthly_engagement_score_x'] = row['monthly_engagement_score_y']
    elif row['monthly_engagement_score_y'] == 0:
        final_frame.at[index, 'monthly_engagement_score_y'] = row['monthly_engagement_score_x']
        
# final_frame.loc[final_frame['monthly_engagement_score_x'] == 0, 'monthly_engagement_score_x'] = final_frame['monthly_engagement_score_y']
# final_frame.loc[final_frame['monthly_engagement_score_y'] == 0, 'monthly_engagement_score_y'] = final_frame['monthly_engagement_score_x']   
