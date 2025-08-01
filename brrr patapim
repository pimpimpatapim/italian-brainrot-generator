import openai
import os

# Imposta la tua API key di OpenAI qui o usa la variabile d'ambiente OPENAI_API_KEY
openai.api_key = os.getenv("OPENAI_API_KEY", "INSERISCI_LA_TUA_API_KEY_QUI")

def genera_personaggio_brainrot_italiano():
    prompt = (
        "Genera un personaggio assurdo e divertente nello stile 'brainrot', tipico dei meme italiani. "
        "Descrivi: nome, tratto principale, frase tipica, cibo preferito e hobby. "
        "Scrivi tutto in italiano e rendilo breve e surreale."
    )
    response = openai.ChatCompletion.create(
        model="gpt-3.5-turbo",  # O usa "gpt-4" se disponibile
        messages=[
            {"role": "user", "content": prompt}
        ],
        max_tokens=150,
        temperature=0.9,
        n=1
    )
    return response['choices'][0]['message']['content']

if __name__ == "__main__":
    print(genera_personaggio_brainrot_italiano())
