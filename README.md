📡 តួនាទីសំខាន់របស់កូដនេះ
✅ 1. បើកដំណើរការ radios និងប្ដូរឆានែលដោយលំដាប់
ប្រើ RF24 radio 2 គ្រឿង (quantumRadio, doomRadio) ដើម្បីបញ្ជូនសញ្ញា RF។

វាប្ដូរឆានែល (channels 0–125) ដោយ sequentiation បែប pattern (ជាសំឡេង jam មិនអាចទទួលបាន properly) ។

✅ 2. ប្រើប៊ូតុងដើម្បីជ្រើសរើសរបៀបផ្លាស់ប្ដូរឆានែល (mode switching)
ប៊ូតុងផ្សេងៗត្រូវបានប្រើសម្រាប់បើក:

Apocalypse Switch: ដាក់ទៅលេី TOTAL ANNIHILATION mode

Mode Selector: ប្តូរទៅ mode បន្ទាប់

Overdrive Button: បើក mode ដ៏ខ្លាំង OVERDRIVE

Internet Destroyer: បើក INTERNET ANNIHILATION

Call Jammer: បើក CALL JAMMING

✅ 3. របៀបបំផ្លាញផ្សេងៗ (Modes):
ប្រភេទ mode មានអត្តសញ្ញាណដូចជា (ឈ្មោះអាចខ្មៅលើស្តើង 😅 ប៉ុន្តែចំណុចបច្ចេកទេសគឺ...):

Mode	អ្វីដែលវាធ្វើ
QUANTUM ENTANGLEMENT	ប្ដូរឆានែលយ៉ាងលឿន (pattern)
BLACK HOLE	ប្ដូរឆានែលជារបៀបរងធ្ងន់
INTERNET ANNIHILATION	ប្ដូរឆានែលច្រើនគេប្រើ (WiFi-like)
CALL JAMMING	ប្ដូរឆានែលដែលប្រើសម្រាប់ការហៅ
TOTAL ANNIHILATION	ប្ដូរឆានែលទាំងអស់ជាបន្តបន្ទាប់
OVERDRIVE	បញ្ជូន constant carrier power ខ្លាំង

💡 បច្ចេកទេសដែលប្រើ:
RF24 Radios: ប្រើជាមួយ library RF24 ដើម្បីបញ្ជូន/ផ្ទុក signal (Tx only).

ezButton: សម្រាប់ debouncing និងគ្រប់គ្រងប៊ូតុងយ៉ាងឆ្លាតវៃ។

PROGMEM: រក្សា pattern ក្នុង flash memory ជំនួស RAM (ប្រសើរចំពោះ RAM usage)។

Dynamic channel switching: ប្ដូរឆានែលយ៉ាងលឿន ដើម្បីបង្កើត radio interference/jamming effects។

High Frequency Looping: ប្រើ delayMicroseconds() ក្នុង loop ដើម្បីធ្វើការប្ដូរឆានែលក្នុង microseconds level។

❌ តើវាធ្វើ Jamming បានឬទេ?
🔊 នៅពេល មិនមានការស្តាប់សញ្ញា (radio.stopListening()), ហើយប្ដូរឆានែលយ៉ាងលឿន + power level MAX, វាអាចបង្កភាពច្របូកច្របល់លេីឆានែល RF។

👉 វាគ្រាន់តែ broadcast signal នៅ frequency តែប៉ុណ្ណោះ, មិនសូវមាន jamming efficiency លើស WiFi/LTE/GPS ដូចជា jammer ស្របច្បាប់ពិតៗនោះទេ។ ចំពោះ jammingពិតប្រាកដ វាត្រូវការមាន control signal, timing precision, power amplifier, modulation degradation, និងការប្រើ DAC/ADC ដល់ស្តង់ដារ RF.

⚠️ សម្គាល់សុវត្ថិភាព និងច្បាប់:
ការបញ្ជូនសញ្ញា RF នៅ frequency មិនអនុញ្ញាត ឬដែលអាចរំខានគេ គឺខុសច្បាប់ នៅក្នុងប្រទេសភាគច្រើន។

ចូរប្រើកូដនេះសម្រាប់ សិក្សា RF, simulation, ឬក្នុង Faraday Cage/Test environment ប៉ុណ្ណោះ។

