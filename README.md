from reportlab.pdfgen import canvas

# 9:16 aspect ratio in points (e.g., 612 x 1088)
PAGE_WIDTH = 612
PAGE_HEIGHT = 1088

def generate_pdf(filename="Proof_of_Recovery_yrbestie_9x16.pdf"):
    c = canvas.Canvas(filename, pagesize=(PAGE_WIDTH, PAGE_HEIGHT))

    c.setFont("Helvetica-Bold", 16)
    c.drawCentredString(PAGE_WIDTH / 2, PAGE_HEIGHT - 60, "Proof of Recovery - Instagram Account")

    c.setFont("Helvetica", 11)
    text = c.beginText(40, PAGE_HEIGHT - 100)

    lines = [
        "Date of Recovery: 02 May 2025",
        "Account Username: @yrbestie",
        "Account Owner: yrbestie",
        "Recovery Conducted by: Rileythedev (Ethical Hacker)",
        "",
        "Incident Summary:",
        "On or prior to 02 May 2025, the Instagram account @yrbestie was either compromised due to",
        "unauthorized access (hacked) or permanently banned due to suspected violations of Instagram's Terms of Service.",
        "",
        "Symptoms Observed:",
        "- Loss of account access",
        "- Altered account details and/or suspicious activity",
        "- Possible content violations leading to ban or restriction",
        "",
        "Recovery Actions Taken:",
        "1. Confirmed rightful ownership through secure identity verification.",
        "2. Filed an official appeal or recovery request with Instagram’s support team.",
        "3. Provided necessary documentation and account history to validate ownership.",
        "4. Regained access on 02 May 2025 after completing platform security protocols.",
        "5. Implemented critical security measures including:",
        "   - Password reset",
        "   - Two-factor authentication (2FA)",
        "   - Verified email and phone number updates",
        "",
        "Outcome:",
        "The account was successfully recovered and all unauthorized access or restrictions were resolved.",
        "The account is now secured under the rightful ownership of @yrbestie.",
        "",
        "Signed,",
        "Rileythedev",
        "Ethical Hacker / Recovery Specialist"
    ]

    for line in lines:
        text.textLine(line)

    c.drawText(text)
    c.save()
    print(f"PDF saved as: {filename}")

generate_pdf()
