https://stackoverflow.com/a/64016190/6615163

for index, row in final_frame.iterrows():
    if row['score_x'] == 0:
        final_frame.at[index, 'score_x'] = row['score_y']
    elif row['score_y'] == 0:
        final_frame.at[index, 'score_y'] = row['score_x']
        
# final_frame.loc[final_frame['score_x'] == 0, 'score_x'] = final_frame['score_y']
# final_frame.loc[final_frame['score_y'] == 0, 'score_y'] = final_frame['score_x']   
