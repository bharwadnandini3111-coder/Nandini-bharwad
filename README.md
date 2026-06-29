def detect_phishing(email_text):
    phishing_keywords = [
        "urgent", "verify", "password", "otp",
        "bank", "click here", "login", "account suspended"
    ]

    email = email_text.lower()

    for word in phishing_keywords:
        if word in email:
            return "⚠️ Warning: This email may be a phishing email."

    return "✅ No obvious phishing signs found."

# Example
email = input("Enter email text: ")
print(detect_phishing(email))
