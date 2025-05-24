from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def home():
    return render_template('index.html')

@app.route('/zmist')
def zmist():
    return render_template('zmist.html')

@app.route('/modul1')
def modul1():
    return render_template('modul1.html')

@app.route('/tema1')
def tema1():
    return render_template('tema1.html')

@app.route('/tema2')
def tema2():
    return render_template('tema2.html')

@app.route('/tema3')
def tema3():
    return render_template('tema3.html')

@app.route('/p1')
def p1():
    return render_template('p1.html')

@app.route('/p2')
def p2():
    return render_template('p2.html')

@app.errorhandler(404)
def page_not_found(e):
    return render_template('404.html'), 404

if __name__ == '__main__':
    app.run(port=8000, debug=True)
