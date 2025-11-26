# How to Sync This Project to Snowflake Workspaces

## Quick Steps:

### Option 1: Clone in Snowflake Workspaces (Recommended)
1. Log into your Snowflake account: `SYBTQPP-WTB85685.snowflakecomputing.com`
2. Navigate to **Workspaces** (left sidebar)
3. Click **"New Workspace"** or **"Create Workspace"**
4. In the Git repository field, enter:
   ```
   https://github.com/Snowflake-Labs/getting-started-with-dbt-on-snowflake.git
   ```
5. Click **Clone** or **Create**
6. Once cloned, navigate to the `tasty_bytes_dbt_demo` folder
7. Run: `dbt deps` (to install packages)
8. Run: `dbt debug` (to test connection - Snowflake Workspaces handles auth automatically)

### Option 2: Manual File Copy
If you already have a workspace:
1. Open your Snowflake Workspace
2. Create a folder called `tasty_bytes_dbt_demo` (if it doesn't exist)
3. Copy all files from this local folder to the workspace folder
4. Make sure to copy:
   - `dbt_project.yml`
   - `packages.yml`
   - `models/` folder
   - `macros/` folder
   - `tests/` folder
   - `setup/` folder
5. Run `dbt deps` in the workspace

## Project Details:
- **Project Name**: `tasty_bytes`
- **Profile Name**: `tasty_bytes`
- **Database**: `TASTY_BYTES_DBT_DB`
- **Schema**: `DEV`
- **Warehouse**: `TASTY_BYTES_BDT_WH`

## Notes:
- Your local `profiles.yml` contains credentials and won't sync (that's good!)
- Snowflake Workspaces uses automatic authentication
- The `dbt_packages/` folder will be recreated when you run `dbt deps` in Snowflake

