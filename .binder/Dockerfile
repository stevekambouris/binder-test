FROM rocker/binder:3.4.0
LABEL maintainer='Steven Kambouris'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}

RUN R -e "remotes::install_version('metafor', '1.9-6', repos = 'https://cran.ms.unimelb.edu.au')"

#RUN wget https://github.com/karthik/binder-test/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-10-24/')); devtools::install_deps()"

#RUN rm DESCRIPTION.1; exit 0
