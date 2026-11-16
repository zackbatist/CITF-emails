# CITF-emails

Exploratory analysis of emails generated throughout the CITF Databank's operations.

To preview the site locally:

1. Download and install Quarto.
2. Clone this repo and cd into it.
3. Use `quarto preview`.
4. Navigate to localhost:7777 in your web browser.

## Running the notebooks

The notebooks run on the CITF analysis server and share one environment, built from `requirements.txt`:

```
python3.12 -m venv ~/citf-emails-env
~/citf-emails-env/bin/pip install -r requirements.txt
~/citf-emails-env/bin/python -m ipykernel install --user --name citf-emails-env --display-name citf-emails-env
~/citf-emails-env/bin/nbstripout --install
```

The last command makes git strip notebook outputs, which hold email text, from every commit. In VSCode, select the kernel through Jupyter Kernel and then citf-emails-env.