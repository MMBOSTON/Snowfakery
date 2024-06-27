# 2024.06.05

conda create --name snowfakery_env python=3.12.3
conda activate snowfakery_env

pip install markdown-it-py numpy scipy packaging Pygments
pip install snowfakery 
pip install sqlalchemy

Dry Run to see the output in Terminal window:
>snowfakery cs_health_dashboard.yaml   (Datamodel Recipe file) ###Tesing the YAML file syntax

>snowfakery --output-format SQL --output-file cs_health_dashboard_db1.sql cs_health_dashboard.yaml

install SQLite3 and ensure it's added to your system's PATH. Here are the steps to do this:

1. Download the SQLite3 from the official SQLite website: https://www.sqlite.org/download.html
2. Extract the downloaded file.
3. Add the extracted directory to your system's PATH.

To add the directory to your system's PATH on Windows:

1. Right-click on 'Computer' and click on 'Properties'.
2. Click on 'Advanced System Settings'.
3. Click on 'Environment Variables'.
4. Under 'System Variables', find the PATH variable, select it, and click on 'Edit'.
5. In the 'Variable value' field, append the path of the extracted SQLite directory to the existing value. Make sure to separate it with a semicolon (;).
6. Click 'OK' to close all dialog boxes.

C:\ProgramData\Microsoft\Windows\Start Menu\Programs\SQLiteStudio

Download sqlite3 and watch the video https://youtu.be/XA3w8tQnYCA?si=VnkJVo2k1uUanQIi

sqlite3 --version 
sqlite3 cs_health_dashboard.db < cs_health_dashboard_db1.sql

#########################################################

1. Open the terminal in Visual Studio Code.

2. Create a new conda environment. Replace `snowfakery_env` with the name you want for your environment.

```bash
conda create --name snowfakery_env python=3.8
```

3. Activate the new environment.

```bash
conda activate snowfakery_env
```

4. Install some dependencies
pip install markdown-it-py numpy scipy packaging Pygments

4. Install Snowfakery using pip.

```bash
pip install snowfakery
```

5. Now, you can use a YAML recipe file to run Snowfakery. Here's an example command, replace `your_recipe.yaml` with your actual file name.

```bash
snowfakery your_recipe.yaml
```

6. If you want to output the generated data to a SQL database, you can use the `--output-format` and `--output-file` options. Here's an example command that outputs to a SQLite database.

```bash
snowfakery --output-format sqlite --output-file output.db your_recipe.yaml
```

7. To interact with the SQLite database, you might want to install a SQLite database browser. Here's how to install the `sqlite3` command-line utility using conda.

```bash
conda install -c anaconda sqlite
```

8. Now, you can use the `sqlite3` command to interact with your SQLite database. Here's an example command that opens the SQLite database in the terminal.

```bash
sqlite3 output.db
```

Remember to replace `output.db` with your actual database file name in the above commands.