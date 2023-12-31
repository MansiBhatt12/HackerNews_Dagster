# Dagster_tutorial_project

This is a [Dagster](https://dagster.io/) project scaffolded with [`dagster project scaffold`](https://docs.dagster.io/tutorial).

## Getting started

First, install your Dagster code location as a Python package.["To install Python, pip and to setup virtual environment."](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/) so that as you develop, local code changes will automatically apply.

Clone this repository to the directory where you setup your python virtual environment.

[Activate your virtual environment]
```bash
source path/to/venv/bin/activate
```

Navigate to the directory- tutorial-project

[To install Dagster and Dagit]
```bash
pip install dagster dagit
```

```bash
pip install -e ".[dev]"
```

Then, start the Dagster UI web server:

```bash
dagster dev
```

Open http://localhost:3000 with your browser to see the project.

You can start writing assets in `tutorial_project/assets.py`. The assets are automatically loaded into the Dagster code location as you define them.

## Note 
Don't forget to import, install necessary packages 

```bash
pip install package_name
```

## Development


### Adding new Python dependencies

You can specify new Python dependencies in `setup.py`.

### Unit testing

Tests are in the `tutorial_project_tests` directory and you can run tests using `pytest`:

```bash
pytest tutorial_project_tests
```

### Schedules and sensors

If you want to enable Dagster [Schedules](https://docs.dagster.io/concepts/partitions-schedules-sensors/schedules) or [Sensors](https://docs.dagster.io/concepts/partitions-schedules-sensors/sensors) for your jobs, the [Dagster Daemon](https://docs.dagster.io/deployment/dagster-daemon) process must be running. This is done automatically when you run `dagster dev`.

Once your Dagster Daemon is running, you can start turning on schedules and sensors for your jobs.

## Deploy on Dagster Cloud

The easiest way to deploy your Dagster project is to use Dagster Cloud.

Check out the [Dagster Cloud Documentation](https://docs.dagster.cloud) to learn more.
