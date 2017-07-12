FROM jupyter/base-notebook

# Additional Conda packages
RUN conda install --quiet --yes \
    'pandas=0.19*' \
    'pymysql=0.7.9' \
    'sqlalchemy=1.1*' \

    && conda clean -tipsy

