# Databricks Asset Bundles
```shell
brew tap databricks/tap
brew install databricks
```

# Step 1: Set Up Authentication
```shell
databricks -v
databricks auth login --host https://adb-2090585310411504.4.azuredatabricks.net/ --profile development
databricks auth profiles
```

# Step 2: Create Bundle [dab_uber_eats]
```shell
databricks bundle init
```

# Step 3: Deploy Local Project to Remote Workspace
```shell
databricks bundle validate
databricks bundle deploy -t dev
```

# Step 4: Run Deployed Project
```shell
databricks bundle run -t dev dab_uber_eats_pipeline
```

# Step 5: Clean Up
```shell
databricks bundle destroy -t dev
```
