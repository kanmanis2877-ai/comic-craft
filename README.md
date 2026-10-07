Last one da! Final touch! 🎨

### PROJECT 5: ComicCraft - AI Comic Story Creator

*GitHub Repo Name:* `ComicCraft-AI`

*1. http://app.py:*
import streamlit as st
import google.generativeai as genai

genai.configure(api_key="YOUR_GEMINI_API_KEY")
model = genai.GenerativeModel("gemini-1.5-flash")

st.set_page_config(page_title="ComicCraft", page_icon="🎨")
st.title("🎨 ComicCraft - AI Comic Story Creator")
st.markdown("Turn your idea into a comic story in 10 seconds!")

idea = st.text_input("Comic Idea Enna? (Ex: A dog who becomes Chennai auto driver)", "A robot explores Kulittalai")
characters = st.text_input("Main Characters", "Robot Robo, Little boy Arjun")
style = st.selectbox("Art Style", ["Cute Cartoon", "Anime", "Marvel Superhero", "Chibi", "Manga"])
language = st.selectbox("Story Language", ["Tanglish", "English", "Tamil"])

panels = st.slider("How many panels?", 3, 6, 4)

if st.button("✨ Create Comic Story"):
    if idea:
        with st.spinner("Comic sketch panrom..."):
            prompt = f"""
            You are ComicCraft AI. Create a {panels}-panel comic story.
            Idea: {idea}
            Characters: {characters}
            Art Style: {style}
            Language: {language}
            For each panel give:
            Panel [number]:
            - Visual Description: (for image generation, detailed prompt)
            - Dialogue / Caption: funny, short
            - Mood: e.g., funny, exciting
            At end, give a moral of the story.
            """
            res = model.generate_content(prompt)
            st.success(f"{panels} Panel Comic Ready!")
            st.write(res.text)
            st.info("💡 Tip: Visual Description ah copy panni Gemini / Imagen / Leonardo AI la paste panni image generate pannalam!")
            st.snow()
    else:
        st.warning("Idea sollu da!")

st.sidebar.markdown("""
**How to add images:**
1. Copy Visual Description
2. Go to aistudio.google.com -> Image Gen
3. Paste & generate
4. Upload here (future version)

**For NASSCOM FSP Project**
""")
*2. http://requirements.txt:*
streamlit
google-generativeai
*3. http://README.md:*
# ComicCraft - AI Comic Story Creator
SB Generative AI with Google Cloud Data
- Converts idea to 4-6 panel comic script
- Gives visual prompts for image generation
- Tanglish support
Future: Image generation integration
---

### ✅ ELLAM MUDINJUTHU DA!

Ipo un kitta 5 project um full ready:

1. EduGenie-Gemini ✅
2. LegalEase-AI ✅
3. PocketSmart-AI ✅
4. FitBuddy-Gemini ✅
5. ComicCraft-AI ✅

*Final Step - GitHub la epdi podanum:*
1. http://github.com la poi 5 repo create pannu (pera mela irukkura maathiri)
2. Antha http://app.py code la `YOUR_GEMINI_API_KEY` ku bathila un Gemini Key ah podu (aistudio.google.com)
3. SkillWallet -> Project Assets la antha 5 GitHub link ah paste pannidu

Oru doubt na kooda, screenshot anuppu, naan paathu solluren. All the best da! 5 team kum full marks thaan!
