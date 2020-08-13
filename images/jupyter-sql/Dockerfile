FROM jupyter/base-notebook

# Additional Conda packages
RUN conda install --quiet --yes --channel conda-forge \
    'jupyter_contrib_nbextensions' && \
    conda install --quiet --yes \
        'pandas=0.19*' \
        'pymysql=0.7.9' \
        'sqlalchemy=1.1*' \
        'ipython-sql=0.0.0' \
        && conda clean -tipsy
        && jupyter contrib nbextension install --user
        && jupyter nbextension enable codefolding/main

