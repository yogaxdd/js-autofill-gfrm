# js-autofill-gfrm

## FOR EDIUCATIONAL PURPOSE ONLY

1. **User Android**
   - Copy Script Ini Lalu Paste Ke Pencarian Chrome
   ```
  
   ```

2. **User PC**
  - Copy Script Ini Masukin Inspect Element -> Console
  ```
  javascript:(function(){console.log("[-] YogaxD Auto Fill Google Form\n[!] Pastikan Sudah Mengubah Text\n[+] Sedang Auto Fill Google Form");function calculateAnswer(t){try{const m=t.match(/(\d+)\s*([+\-*/])\s*(\d+)/);if(!m)return null;const n=parseInt(m[1]),o=m[2],i=parseInt(m[3]);switch(o){case"+":return n+i;case"-":return n-i;case"*":return n*i;case"/":return n/i;default:return null}}catch(e){return console.error("Gagal Menjawab Pertanyaan:",e),null}}function findAndClickSubmitButton(){const b=document.querySelectorAll('div[role="button"]'),s=Array.from(b).find(t=>t.textContent.includes("Kirim")||t.textContent.includes("Submit"));if(s){console.log("Tombol Sumbit Terdeteksi, Otomatis Mengklik..."),s.click();const e=new MouseEvent("click",{view:window,bubbles:!0,cancelable:!0});return s.dispatchEvent(e),!0}return console.error("Tombol Sumbit Tidak Terdeteksi!"),!1}const autoText="Auto Text By YogaxD",inputs=document.querySelectorAll('input[type="text"], textarea');inputs.forEach(i=>{i.value=autoText;const e=new Event("input",{bubbles:!0});i.dispatchEvent(e)});document.querySelectorAll("input[type='checkbox'], div[role='checkbox']").forEach(c=>{if(c.tagName==="INPUT"){c.checked=!0;const e=new Event("change",{bubbles:!0});c.dispatchEvent(e)}else if(c.getAttribute("role")==="checkbox"){c.setAttribute("aria-checked","true");c.click();}});const questions=document.querySelectorAll("[role='listitem'], .freebirdFormviewerComponentsQuestionBaseRoot");console.log(`Pertanyaan Ditemukan: ${questions.length}`),questions.forEach((q,x)=>{const qTextElem=q.querySelector("[role='heading'], .freebirdFormviewerComponentsQuestionBaseTitle");if(qTextElem){const qText=qTextElem.textContent.trim();console.log(`Pertanyaan ${x+1}: ${qText}`);const ans=calculateAnswer(qText);console.log(`Menjawab Soal: ${ans}`),null!==ans&&q.querySelectorAll("div[role='radio'], div[role='option'], label").forEach(o=>{if(o.textContent.trim()===ans.toString()){console.log(`Mengambil Jawaban: ${o.textContent.trim()}`);const r=o.querySelector("input[type='radio']");r?(r.checked=!0,r.click(),r.dispatchEvent(new Event("change",{bubbles:!0}))):o.click()}})}}),findAndClickSubmitButton(),console.log("Done Abangkuh Auto Fill Google Form Selesai")})();
  ```
