FROM jupyter/scipy-notebook:latest

RUN pip install --no-cache-dir -r requirements.txt

# 复制所有文件到 /home/jovyan/work
COPY ./netebook /home/jovyan/work
COPY ./results /home/jovyan/work

# 设置工作目录，使 Jupyter 直接打开 /home/jovyan/work
WORKDIR /home/jovyan/work

# 确保 Notebook 启动目录正确
CMD ["start-notebook.sh", "--NotebookApp.token=''"]
