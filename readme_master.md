create an env file and install the dependencies there
the env that I worked for this demo is 'openai'

step 1, create a virtual env and activate it

    use cmd not powershell
    pip install virtualenv
    python -m virtualenv env --python=python3.9
    use cmd
    .\env\Scripts\activate

step 2, change route

    cd server

step 3, install package

    pip install -r requirements.txt

step 4, update config file with local ip address

    ipconfig

step 5, start flask first (user your device ip for --host)

    set FLASK_APP=run.py
    set ENV=development
    flask run --host 192.168.1.24 --port 5000
    or
    $env:FLASK_APP = "run.py"
    $env:FLASK_ENV = "development"
    flask run
    or

step 6, start another cmd and run the streamlitapp

    cd server
    streamlit run app.py

if you add new context to the huanan_result_clear.xlsx
please delete the faiss_store folder and restart

General questions:

Who did the process improvement of line one?
Check Jupyter kernel list present in the windows

    .\env\Scripts\activate
    python -m ipykernel install --user --name=sqlqa
    jupyter kernelspec list
