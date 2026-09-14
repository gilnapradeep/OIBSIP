# Inference pipeline function
def predict_message(text, model=nb_model, vectorizer=tfidf):
    processed = vectorizer.transform([text])
    pred = model.predict(processed)[0]
    prob = model.predict_proba(processed)[0][pred]
    label = "SPAM" if pred == 1 else "HAM (Legitimate)"
    return label, prob

# Test cases
sample_messages = [
    "Hey, are we still meeting up for coffee tomorrow afternoon?",
    "URGENT! You have won a 1000 cash prize or a free holiday. Call 09050000321 to claim your reward now!",
    "Can you please review the attached report before Monday's presentation?",
    "Congratulations! You are selected for an exclusive credit loan with 0% interest. Click here to register."
]

print("--- Real-time Message Predictions ---")
for msg in sample_messages:
    label, confidence = predict_message(msg)
    print(f"\nMessage: \"{msg}\"")
    print(f"Classification: [{label}] (Confidence: {confidence*100:.2f}%)")