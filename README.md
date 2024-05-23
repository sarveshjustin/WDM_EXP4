```python
# read the data
import pandas as pd
visitor_df = pd.read_csv('/content/clustervisitor.csv')
age_groups = {
    'Young': visitor_df['Age'] <= 30,
    'Middle-aged': (visitor_df['Age'] > 30) & (visitor_df['Age'] <= 50),
    'Elderly': visitor_df['Age'] > 50
}

for group, condition in age_groups.items():  
    visitors_in_group = visitor_df[condition] 
    print(f"Visitors in {group} age group:")
    print(visitors_in_group)

visitor_counts=[]
for group,condition in age_groups.items():
  visitors_in_group=visitor_df[condition]
  visitor_counts.append(len(visitors_in_group))
    
age_group_labels=list(age_groups.keys())
```
### Output:
![311411222-54cc6e89-2b8b-4245-9ae0-9f3536209c4f](https://github.com/Vineesh-AI-DS/WDM_EXP4/assets/93427254/9e51645f-0f06-4c5b-8216-5dfbb126b2a4)

### Result:
Thus the cluster and visitor segmentation for navigation patterns was implemented successfully in python.
