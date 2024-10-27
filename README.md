# app.py

from flask import Flask, request, jsonify

app = Flask(__name__)

@app.route('/generate', methods=['POST'])
def generate_text():
    user_input = request.json.get('text')
    
    # Yahan tumhare AI model ko text bhejne ka process hoga, yahan main ek simple response de raha hoon.
    response = "AI generated content based on your input: " + user_input
    
    return jsonify({"response": response})

if __name__ == '__main__':
    app.run(debug=True)
