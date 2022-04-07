FROM armswdev/tensorflow-arm-neoverse:r22.04-tf-2.8.0-onednn-acl

RUN pip uninstall -y scikit-learn
RUN pip install scikit-learn===1.0.2 jupyterlab===3.4.0 librosa===0.9.1
RUN mkdir techday-music

WORKDIR techday-music

ENV LD_PRELOAD="/home/ubuntu/python3-venv/lib/python3.8/site-packages/scikit_learn.libs/libgomp-d22c30c5.so.1.0.0:${LD_PRELOAD}"

ENTRYPOINT ["jupyter", "lab", "--ip=\"0.0.0.0\"", "--NotebookApp.iopub_data_rate_limit=1.0e10"]
