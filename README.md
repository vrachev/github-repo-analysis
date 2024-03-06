
# Github Repo Analysis

A small project looking into the 127k Github repos between 2019-2023 that have been starred at least 100 times. `visualize_repos.ipynb` is the notebook containing all visualizations. The json files are too big to drop into the repo, so I'm hosting them in my [Google drive](https://drive.google.com/drive/folders/1_Db8GW5OYF1E229LV3_LV7gGvLkupH7Z?usp=drive_link).

## The Data

The data was gathered using Github's search API. It's a point in time snapshot, so the charts and tables will lose accuracy over time as the underlying data changes.

In addition to the repo fields returned by Github, I also added two fields, which I used for some charts around repo activity.
```python
   since_commit: int # days since last commit, computed as current-time - repo.pushed_at
   active: bool # true if since_commit > 30
```

## Set up

To run the `visualize_repos.ipynb` notebook, you need to set up a Python virtual environment and install the necessary packages. Follow these steps to get started:

1. Download the [repo.json files](https://drive.google.com/drive/folders/1_Db8GW5OYF1E229LV3_LV7gGvLkupH7Z?usp=drive_link)
2. Create a venv
   ```
   python -m venv venv
   ```
3. Activate the virtual environment by running:
   ```
   source venv/bin/activate
   ```
4. Install the required packages using:
   ```
   pip install -r requirements.txt
   ```
5. Start jupyter:
   ```
   jupyter lab
   ```
6. Some times jupyter fails to pick up the venv, this may fix this:
   ```
   python -m ipykernel install --user --name=venv
   ```

