================
PHI Masker Utils
================


Collection of Python modules for masking PHI in delimited files and Excel worksheets.

Usage
-----

.. code-block:: python

    from phi_masker_utils import Masker

    config_file = "conf/config.yaml"
    config = yaml.safe_load(Path(config_file).read_text())

    # Tab-delimited file
    infile = "my.tsv"
    outfile = "my_masked.tsv"

    # Or comma-separated file
    infile = "my.csv"
    outfile = "my_masked.csv"

    masker = Masker(
        config=config,
        config_file=config_file,
        infile=infile,
        logfile=logfile,
        outdir=outdir,
        outfile=outfile,
        verbose=verbose,
    )

    masker.mask_phi_values()

Exported Script
---------------

.. code-block:: shell

    mask-file --infile ~/projects/phi-masker-utils/labguru_mockup.csv --outdir .
    --config_file was not specified and therefore was set to 
    '/tmp/phi-masker-utils/venv/lib/python3.10/site-packages/phi_masker_utils/conf/config.yaml'
    --logfile was not specified and therefore was set to './mask_file.log'
    --outfile was not specified and therefore was set to './labguru_mockup.csv'
