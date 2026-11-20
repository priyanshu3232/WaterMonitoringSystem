Jal Nigrani

Drinking water quality monitoring and corrective action tracker for Khagaria district, Bihar (prototype)

Jal Nigrani follows every water sample from collection to the point where the people using that source have safe water again. It was built as part of an internship project with the Public Health Engineering Department (PHED), Khagaria.

This is a prototype with sample data. It is not an official government website. All names, phone numbers, sources and results in it are sample values.

Live demo: https://<your-project>.vercel.app (replace with your Vercel link)

The problem

A water test report alone does not protect anyone. After an adverse result, officials need to find the source, know who depends on it, arrange a response, inform people, test again and confirm that the problem is solved. Jal Nigrani keeps all of this in one record per water source.

Features
Four roles: field staff, lab staff, block officer (Junior Engineer) and DM office
Sample entry in three steps: choose source, test with a field kit or send to a lab, save
Sample tracking: sent, received by lab, result entered
Unique source ID with GPS, households and photos
Automatic case when a result is adverse or severe, with six tracked steps:
Officer takes charge
Repair work started
Other safe water arranged and checked (tested, working, reachable)
People informed
Repeat test is normal
Case closed by the officer
Nearby safe water: lists the five nearest sources with a normal result and their distance
DM dashboard: summary numbers, late cases with the officer to call, block-wise status and stage-wise view of open cases
Map: sources by latest result, dot size by households, zoom and drag
Tickets: any user can raise a problem and assign it to a person
Source history: every sample, result and action, with the next test date
Hindi and English, with a text size control
Demo logins

The login page fills these in automatically for the role and block you choose.

Role	User ID	Password
Field staff	fs_ + block name, for example fs_gogri	field@123
Block officer	je_ + block name, for example je_gogri	je@123
Lab staff	lab_khagaria, lab_chautham, lab_gogri	lab@123
DM office	dm_khagaria	dm@123

Blocks: Alauli, Khagaria, Chautham, Mansi, Gogri, Beldaur, Parbatta.

Run it

The whole prototype is one file, index.html. There is no build step.

Locally: open index.html in a browser.
On Vercel: import this repository, keep the framework preset as "Other", leave the build command empty and deploy.
Limits of this prototype
Data stays in one browser. It is saved in the browser's local storage, so each visitor sees their own copy. Use "Reset sample data" on the login page to start again.
The login is a demonstration. User IDs and passwords are inside the page. It is not real security.
GPS is typed by hand. A production app would read it from the phone.
Water-quality limits and time limits are placeholders. PHED has to confirm them before any field use.
Sample data only. The seven blocks and three laboratories are real. Sources, households, results, officers and phone numbers are not.
Tech
Plain HTML, CSS and JavaScript in a single file
No framework and no backend
Fonts: DM Sans and Noto Sans Devanagari from Google Fonts
Planned next
Rebuild in React with a backend and a shared database
Real user accounts issued by the DM office
Automatic GPS capture on mobile
Pilot in selected habitations with real sources and cases
