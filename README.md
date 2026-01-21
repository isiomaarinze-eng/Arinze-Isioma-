# Arinze-Isioma-
Dictionary 
```json
   {
       "hello": "bawo",
       "thank you": "eshe",
       "goodbye": "o dabọ",
       "please": "jowo",
       "yes": "beeni",
       "no": "rara",
       "friend": "ore",
       "family": "ebi",
       "love": "ifẹ",
       "water": "omi",
       "food": "ounje",
       "house": "ile",
       "school": "ile-iwe",
       "book": "iwe",
       "car": " ọkọ ayọkẹlẹ",
       "money": "owo",
       "work": "ise",
       "time": "akoko",
       "day": "ojo",
       "night": "oru"
   }```python
   import json

   def load_dictionary(language):
       with open(f'{language}.json', 'r', encoding='utf-8') as file:
           return json.load(file)

   def translate(word, dictionary):
       return dictionary.get(word.lower(), "Translation not found.")

   def main():
       languages = ['yoruba']  # Add your language files
       print("Available languages:", languages)
       chosen_language = input("Choose a language: ")
       
       if chosen_language in languages:
           dictionary = load_dictionary(chosen_language)
           word_to_translate = input("Enter an English word to translate: ")
           translation = translate(word_to_translate, dictionary)
           print(f'Translation: {translation}')
       else:
           print("Language not found.")

   if __name__ == "__main__":
       main()
   ```
