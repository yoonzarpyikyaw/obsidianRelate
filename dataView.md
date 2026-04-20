Dataview plugin ဟာ Obsidian ရဲ့ အစွမ်းထက်ဆုံး Plugin တစ်ခုဖြစ်ပြီး သင့် Vault ထဲက Note တွေကို Database တစ်ခုလိုမျိုး Table (ဇယား)၊ List (စာရင်း) တွေနဲ့ အလိုအလျောက် ပြန်ထုတ်ပြပေးနိုင်ပါတယ်။

သင်လိုချင်တဲ့ Password folder ထဲက data တွေကိုပဲ သီးသန့်ကြည့်ဖို့အတွက် Dataview က အကောင်းဆုံးပါပဲ။ အသုံးပြုနည်း အခြေခံကို အောက်မှာ ရှင်းပြပေးထားပါတယ်။

၁။ အခြေခံ Syntax (ရေးထုံး)
Dataview ကို အသုံးပြုဖို့အတွက် Note တစ်ခုထဲမှာ Code block ပုံစံမျိုး ရေးရပါတယ်။ အခြေခံအားဖြင့် အပိုင်း (၄) ပိုင်း ပါဝင်ပါတယ် -

```
Code snippet
TABLE field1, field2
FROM "folder-name"
WHERE condition
SORT field1 ASC/DESC
```
၂။ လက်တွေ့အသုံးပြုနည်း (ဥပမာ)
သင့်မှာရှိတဲ့ password folder ထဲက note တွေကိုပဲ ဇယားနဲ့ ထုတ်ကြည့်ချင်တယ်ဆိုရင် အောက်ပါအတိုင်း ရေးနိုင်ပါတယ် -

```
Table View (ဇယားဖြင့် ကြည့်ခြင်း)
Code snippet
TABLE category, username, last_updated
FROM "password"
```
ဒီ code ကို ရေးလိုက်ရင် "password" folder ထဲမှာရှိတဲ့ note တွေ အကုန်ပေါ်လာမယ်။ category နဲ့ username ဆိုတဲ့ column တွေ ပါလာပါလိမ့်မယ်။

```
List View (စာရင်းဖြင့် ကြည့်ခြင်း)
Code snippet
LIST
FROM "password"
WHERE contains(tags, "#important")
```
ဒါကတော့ password folder ထဲက tag မှာ #important ပါတဲ့ note တွေကိုပဲ စာရင်းထုတ်ပေးမှာပါ။

၃။ Note ထဲမှာ Data ထည့်သွင်းပုံ (Properties)
Dataview က data တွေကို ဆွဲထုတ်နိုင်ဖို့အတွက် သင့်ရဲ့ note တွေမှာ Properties (Frontmatter) ထည့်ထားဖို့ လိုပါတယ်။ Note တစ်ခုရဲ့ အပေါ်ဆုံးမှာ အခုလိုမျိုး ရေးရပါတယ် -

Markdown
---
category: Social Media
username: user123
last_updated: 2024-05-20
---
(ဒီလို Properties ထည့်ထားမှသာ Dataview Table ထဲမှာ Column အလိုက် အချက်အလက်တွေ ပေါ်လာမှာ ဖြစ်ပါတယ်)

၄။ Dataview ရဲ့ အားသာချက်များ
အလိုအလျောက် Update ဖြစ်ခြင်း: Folder ထဲကို note အသစ်တစ်ခု ထပ်ထည့်လိုက်တာနဲ့ Dataview table ထဲမှာ အလိုအလျောက် ပေါ်လာပါလိမ့်မယ်။

စစ်ထုတ်နိုင်ခြင်း (Filtering): FROM နေရာမှာ Folder နာမည်သာမက #tag တွေနဲ့လည်း စစ်ထုတ်လို့ ရပါတယ်။

Flexible ဖြစ်ခြင်း: သင်စိတ်ကြိုက် Column တွေ ဆောက်လို့ရသလို၊ ဖိုင်ဆောက်တဲ့ရက်စွဲ (file.ctime) သို့မဟုတ် ပြင်ဆင်တဲ့ရက်စွဲ (file.mtime) တွေနဲ့လည်း Sort လုပ်နိုင်ပါတယ်။

အကြံပြုချက်
Dataview ကို အသုံးမပြုခင် Settings > Community Plugins > Dataview ထဲမှာ Enable JavaScript Queries နဲ့ Enable Inline Queries ကို ဖွင့်ထားဖို့ မမေ့ပါနဲ့။

Dataview ရဲ့ Query ရေးနည်းမှာ အခက်အခဲရှိရင် (ဥပမာ- ရက်စွဲအလိုက် စစ်ထုတ်ချင်တာမျိုး) ထပ်မေးနိုင်ပါတယ်ခင်ဗျာ။ စမ်းရေးကြည့်ချင်တဲ့ query ပုံစံမျိုး ရှိပါသလား?
