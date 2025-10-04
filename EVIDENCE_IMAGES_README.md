# Evidence Image Generation Guide
*Murder at the Ministry - Visual Evidence Creation*

## 🎨 Overview
This script generates professional-quality visual evidence pieces for the Murder at the Ministry mystery game using OpenAI's GPT Image API. Each piece is designed with atmospheric, wizard-world aesthetics matching the game's serious tone.

## 📦 Setup

### 1. Install Dependencies
```bash
pip install openai
```

### 2. Run the Generator

#### Quick Start (Recommended)
```bash
# Fast concurrent generation with auto-retry
./generate_evidence.sh

# Ultra-fast mode (8 parallel workers)
./generate_evidence.sh --fast
```

#### Advanced Options
```bash
# Generate all evidence images (concurrent, 5 workers)
python generate_evidence_images.py

# Generate with custom worker count
python generate_evidence_images.py --workers 8

# Sequential generation (slower but stable)
python generate_evidence_images.py --sequential

# Auto-retry failed images
python generate_evidence_images.py --retry

# Generate a specific evidence piece
python generate_evidence_images.py A1_potion_vial_label
```

### ⚡ Performance Comparison

| Method | Workers | Time Estimate | Stability |
|--------|---------|--------------|-----------|
| Concurrent (default) | 5 | 30-60 seconds | High |
| Fast mode | 8 | 20-40 seconds | Medium |
| Sequential | 1 | 3-5 minutes | Highest |

The concurrent generation is **5-10x faster** than sequential!

## 🖼️ Generated Evidence Pieces

### Round 1 Evidence (Initial Discovery)
- **A1_potion_vial_label** - Torn Transmorph Potion label with partial authorization
- **A2_medical_report** - Official Healer's preliminary examination memo
- **A3_security_log** - Corrupted magical security monitoring data

### Round 2 Evidence (Deeper Investigation)
- **B1_notebook_page** - Victim's paranoid research notes mentioning "R. Kett"
- **B2_wand_analysis** - Forensic spell trace analysis showing unregistered wand
- **B3_burned_message** - Partially destroyed message about the operation
- **B4_apothecary_receipt** - Dark market purchase receipt for R. Kett

### Round 3 Evidence (Final Revelations)
- **C1_temporal_card** - Mystical temporal anomaly detection card
- **C2_mirror_alert** - Security breach notice about Mirror of Masks
- **C3_minister_journal** - Previous Minister's final journal entry
- **C4_unmasking_spell** - Ancient Verum Revelare spell manuscript

### Additional Atmospheric Evidence
- **ministry_seal** - Official wax seal (partially broken)
- **crime_scene_photo** - Victorian magical photograph of the scene
- **transmorph_vial** - Close-up of the color-shifting potion
- **evidence_envelope** - Official evidence storage envelope

## 🎭 Visual Design Philosophy

Each evidence piece is crafted with:

### Authentic Aging Effects
- Torn edges and burn marks
- Coffee stains and water damage
- Crumpled and smoothed textures
- Faded ink and smudged writing

### Magical Elements
- Glowing text and mystical symbols
- Shimmering holographic effects
- Color-shifting liquids
- Ethereal temporal distortions

### Period Aesthetics
- Victorian Gothic typography
- Wax seals and official stamps
- Parchment and aged paper textures
- Fountain pen cursive writing

## 📁 Output Structure

```
evidence_images/
├── A1_potion_vial_label.png
├── A2_medical_report.png
├── A3_security_log.png
├── B1_notebook_page.png
├── B2_wand_analysis.png
├── B3_burned_message.png
├── B4_apothecary_receipt.png
├── C1_temporal_card.png
├── C2_mirror_alert.png
├── C3_minister_journal.png
├── C4_unmasking_spell.png
├── ministry_seal.png
├── crime_scene_photo.png
├── transmorph_vial.png
├── evidence_envelope.png
└── index.html (preview gallery)
```

## 🖨️ Printing Tips

### For Best Results:
1. **Paper:** Use cream or beige cardstock (65-80 lb)
2. **Size:** Images are 1024x1024px for consistent printing
3. **Enhancement:** After printing, lightly tea-stain edges for extra authenticity
4. **Presentation:** Place in aged envelopes or clear protective sleeves

### Print Settings:
- **Quality:** High/Best
- **Color:** Full color (consider slight sepia adjustment)
- **Scale:** Fit to page or actual size
- **Orientation:** Auto-select

## 🎯 Integration with Game

### Evidence Distribution:
1. **Round 1:** Print A1-A3, place in "Evidence A" envelope
2. **Round 2:** Print B1-B4, place in "Evidence B" envelope
3. **Round 3:** Print C1-C4, place in "Evidence C" envelope
4. **Extras:** Use additional pieces for atmosphere or props

### Display Options:
- **Investigation Board:** Pin to corkboard as discovered
- **Evidence Table:** Lay out for examination
- **Individual Handouts:** Pass around during investigation
- **Digital Display:** Show on tablet/laptop if preferred

## 🔧 Customization

### Modify Prompts:
Edit the `EVIDENCE_PIECES` array in `generate_evidence_images.py` to adjust:
- Visual style and atmosphere
- Specific text content shown
- Damage and aging effects
- Magical enhancement levels

### Quality Settings:
```python
# In generate_image() function:
quality="high"  # Options: "low", "medium", "high"
size="1024x1024"  # Options: "1024x1024", "1024x1536", "1536x1024"
```

## 💡 Tips for Success

### API Usage:
- **Concurrent Mode:** Generates up to 5-8 images simultaneously for 5-10x speed boost
- **Auto-retry:** Failed images are automatically retried with `--retry` flag
- **Rate Limiting:** Built-in delays prevent API throttling
- **Single Pieces:** Individual evidence can be regenerated on demand

### Performance Optimization:
- **Default (5 workers):** Best balance of speed and stability
- **Fast Mode (8 workers):** Maximum speed, may hit rate limits
- **Sequential Mode:** Use if experiencing API errors
- **Progress Tracking:** Real-time updates show completion status

### Visual Cohesion:
- All pieces maintain consistent wizard-world aesthetic
- Color palette emphasizes purples, golds, and aged browns
- Lighting suggests mystery and investigation

### Enhanced Immersion:
- Print on textured paper for tactile authenticity
- Use LED candles near evidence for dramatic effect
- Consider laminating frequently-handled pieces
- Create "evidence bags" with case numbers

## 🎨 Preview Gallery

After generation, open `evidence_images/index.html` in your browser to:
- Preview all generated evidence
- Check quality and consistency
- Plan your printing order
- Show players digitally if needed

## ⚠️ Troubleshooting

### If generation fails:
1. Check API key is valid and has credits
2. Ensure internet connection is stable
3. Try regenerating individual pieces
4. Reduce quality setting if timeout occurs

### If images look wrong:
1. Review the prompt for that specific piece
2. Regenerate with adjusted description
3. Try different quality settings
4. Check output resolution matches needs

## 📝 License & Attribution

Images generated using OpenAI's GPT Image API. The game content and prompts are original creative works for the Murder at the Ministry parody game.

---

*"Every piece of evidence tells a story... but not all stories tell the truth."*
