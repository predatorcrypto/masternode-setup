<h1>Predator Masternode Setup Guide (Ubuntu 16.04)</h1>
This guide will assist you in setting up a predatorcoin Masternode on a Linux Server running Ubuntu 16.04. (Use at your own risk)

If you require further assistance contact the support team @ <a href="https://discord.gg/KPsTTAK" rel="nofollow">Discord</a>

<hr />

<h2><a id="user-content-requirements" class="anchor" href="https://github.com/STM0x0/Stim-1#requirements" aria-hidden="true"></a>Requirements</h2>
<ol>
 	<li><strong>5,000 predatorcoin coins.</strong></li>
 	<li><strong>A Vultr VPS running Linux Ubuntu 16.04.</strong></li>
 	<li><strong>A Windows local wallet.</strong></li>
 	<li><strong>An SSH client such as <a href="https://dl.bitvise.com/BvSshClient-Inst.exe" rel="nofollow">Bitvise</a></strong></li>
</ol>

<hr />

<h2><a id="user-content-contents" class="anchor" href="https://github.com/STM0x0/Stim-1#contents" aria-hidden="true"></a>Contents</h2>
<ul>
 	<li><strong>Section A</strong>: Creating the VPS within <a href="https://www.vultr.com/?ref=7296974" rel="nofollow">Vultr</a>.</li>
 	<li><strong>Section B</strong>: Downloading and installing Bitvise.</li>
 	<li><strong>Section C</strong>: Connecting to the VPS and installing the MN script via Bitvise.</li>
 	<li><strong>Section D</strong>: Preparing the local wallet.</li>
 	<li><strong>Section E</strong>: Connecting &amp; Starting the masternode.</li>
</ul>

<hr />

<h2><a id="user-content-section-a-creating-the-vps-within-vultr" class="anchor" href="https://github.com/STM0x0/Stim-1#section-a-creating-the-vps-within-vultr" aria-hidden="true"></a>Section A: Creating the VPS within <a href="https://www.vultr.com/?ref=7296974" rel="nofollow">Vultr</a></h2>
<em><strong>Step 1</strong></em>
<ul>
 	<li>Register at <a href="https://www.vultr.com/?ref=7296974" rel="nofollow">Vultr</a></li>
</ul>

<hr />

<em><strong>Step 2</strong></em>
<ul>
 	<li>After you have added funds to your account go <a href="https://my.vultr.com/deploy/" rel="nofollow">here</a> to create your Server</li>
</ul>

<hr />

<em><strong>Step 3</strong></em>
<ul>
 	<li>Choose a server location (preferably somewhere close to you) <a href="https://camo.githubusercontent.com/726f38950e2f82c45b83f2fb9c3d8ca36bffdb27/68747470733a2f2f692e696d6775722e636f6d2f6f7a6937426b722e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/726f38950e2f82c45b83f2fb9c3d8ca36bffdb27/68747470733a2f2f692e696d6775722e636f6d2f6f7a6937426b722e706e67" alt="Example-Location" data-canonical-src="https://i.imgur.com/ozi7Bkr.png" /></a></li>
</ul>

<hr />

<em><strong>Step 4</strong></em>
<ul>
 	<li>Choose a server type: Ubuntu 16.04 <a href="https://camo.githubusercontent.com/88246bd470b091bf8318ee450db4dde8f9185b94/68747470733a2f2f692e696d6775722e636f6d2f61534d7148554b2e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/88246bd470b091bf8318ee450db4dde8f9185b94/68747470733a2f2f692e696d6775722e636f6d2f61534d7148554b2e706e67" alt="Example-OS" data-canonical-src="https://i.imgur.com/aSMqHUK.png" /></a></li>
</ul>

<hr />

<em><strong>Step 5</strong></em>
<ul>
 	<li>Choose a server size: $5/mo will be fine <a href="https://camo.githubusercontent.com/6efcd9f23f6ddf7ca046ee39e361597b691a192e/68747470733a2f2f692e696d6775722e636f6d2f556f476f48634d2e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/6efcd9f23f6ddf7ca046ee39e361597b691a192e/68747470733a2f2f692e696d6775722e636f6d2f556f476f48634d2e706e67" alt="Example-OS" data-canonical-src="https://i.imgur.com/UoGoHcM.png" /></a></li>
</ul>

<hr />

<em><strong>Step 6</strong></em>
<ul>
 	<li>Set a Server Hostname &amp; Label (name it whatever you want) <a href="https://camo.githubusercontent.com/a3a8e68d8e0f46b1b32bd09dfcb1adc21af42923/68747470733a2f2f692e696d6775722e636f6d2f75753072764f722e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/a3a8e68d8e0f46b1b32bd09dfcb1adc21af42923/68747470733a2f2f692e696d6775722e636f6d2f75753072764f722e706e67" alt="Example-hostname" data-canonical-src="https://i.imgur.com/uu0rvOr.png" /></a></li>
</ul>

<hr />

<em><strong>Step 7</strong></em>
<ul>
 	<li>Click "Deploy now"</li>
</ul>
<a href="https://camo.githubusercontent.com/6e59f5b0bc55bf11db7063400ec2f520e01bbd9b/68747470733a2f2f692e696d6775722e636f6d2f347170597548302e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/6e59f5b0bc55bf11db7063400ec2f520e01bbd9b/68747470733a2f2f692e696d6775722e636f6d2f347170597548302e706e67" alt="Example-Deploy" data-canonical-src="https://i.imgur.com/4qpYuH0.png" /></a>

<hr />

<h2><a id="user-content-section-b-downloading-and-installing-bitvise" class="anchor" href="https://github.com/STM0x0/Stim-1#section-b-downloading-and-installing-bitvise" aria-hidden="true"></a>Section B: Downloading and installing BitVise.</h2>
<em><strong>Step 1</strong></em>
<ul>
 	<li>Download Bitvise <a href="https://dl.bitvise.com/BvSshClient-Inst.exe" rel="nofollow">here</a></li>
</ul>

<hr />

<em><strong>Step 2</strong></em>
<ul>
 	<li>Select the correct installer depending upon your operating system. Then follow the install instructions.</li>
</ul>
<a href="https://camo.githubusercontent.com/8dd1d1119ccfae158da86a0f6e6f7aaa19e8ae89/68747470733a2f2f692e696d6775722e636f6d2f794633363934472e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/8dd1d1119ccfae158da86a0f6e6f7aaa19e8ae89/68747470733a2f2f692e696d6775722e636f6d2f794633363934472e706e67" alt="Example-PuttyInstaller" data-canonical-src="https://i.imgur.com/yF3694G.png" /></a>

<hr />

<h2><a id="user-content-section-c-connecting-to-the-vps--installing-the-mn-script-via-bitvise" class="anchor" href="https://github.com/STM0x0/Stim-1#section-c-connecting-to-the-vps--installing-the-mn-script-via-bitvise" aria-hidden="true"></a>Section C: Connecting to the VPS &amp; Installing the MN script via Bitvise.</h2>
<em><strong>Step 1</strong></em>
<ul>
 	<li>Copy your VPS IP (you can find this by going to the server tab within Vultr and clicking on your server. <a href="https://camo.githubusercontent.com/3794aa2045be353ce1f27394f0adc4f8a6ee066f/68747470733a2f2f692e696d6775722e636f6d2f7a34314d6977592e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/3794aa2045be353ce1f27394f0adc4f8a6ee066f/68747470733a2f2f692e696d6775722e636f6d2f7a34314d6977592e706e67" alt="Example-Vultr" data-canonical-src="https://i.imgur.com/z41MiwY.png" /></a></li>
</ul>

<hr />

<em><strong>Step 2</strong></em>
<ul>
 	<li>Open the bitvise application and fill in the "Hostname" box with the IP of your VPS. <a href="https://camo.githubusercontent.com/1e507520904d317f9f24358f2e44652c4efa986e/68747470733a2f2f692e696d6775722e636f6d2f766b4e31616c432e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/1e507520904d317f9f24358f2e44652c4efa986e/68747470733a2f2f692e696d6775722e636f6d2f766b4e31616c432e706e67" alt="Example-PuttyInstaller" data-canonical-src="https://i.imgur.com/vkN1alC.png" /></a></li>
</ul>

<hr />

<em><strong>Step 3</strong></em>
<ul>
 	<li>Copy the root password from the VULTR server page. <a href="https://camo.githubusercontent.com/5905c8f2c5dd12f5ebe06fce11a1018389290274/68747470733a2f2f692e696d6775722e636f6d2f4a6e58515861762e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/5905c8f2c5dd12f5ebe06fce11a1018389290274/68747470733a2f2f692e696d6775722e636f6d2f4a6e58515861762e706e67" alt="Example-RootPass" data-canonical-src="https://i.imgur.com/JnXQXav.png" /></a></li>
</ul>

<hr />

<em><strong>Step 4</strong></em>
<ul>
 	<li>Type "root" as the login/username. <a href="https://camo.githubusercontent.com/b00482104e5ee6e000ac7eb7b3ff81c0f5042916/68747470733a2f2f692e696d6775722e636f6d2f3131474d6b76412e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/b00482104e5ee6e000ac7eb7b3ff81c0f5042916/68747470733a2f2f692e696d6775722e636f6d2f3131474d6b76412e706e67" alt="Example-Root" data-canonical-src="https://i.imgur.com/11GMkvA.png" /></a></li>
</ul>

<hr />

<em><strong>Step 5</strong></em>
<ul>
 	<li>Paste the password into the Bitvise terminal by right clicking (it will not show the password so just press enter) <a href="https://camo.githubusercontent.com/f08703c7e251c0718e9b55b9257272e2696aca00/68747470733a2f2f692e696d6775722e636f6d2f7a56684f414b752e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/f08703c7e251c0718e9b55b9257272e2696aca00/68747470733a2f2f692e696d6775722e636f6d2f7a56684f414b752e706e67" alt="Example-RootPassEnter" data-canonical-src="https://i.imgur.com/zVhOAKu.png" /></a></li>
</ul>

<hr />

<em><strong>Step 6</strong></em>
<ul>
 	<li>Once you have clicked open it will open a security alert (click yes).</li>
</ul>

<hr />

<em><strong>Step 7</strong></em>
<ul>
 	<li>Paste the code below into the Bitvise terminal then press enter (it will just go to a new line) <a href="https://camo.githubusercontent.com/12693e8705166679a8d41c4989782f3038d53ab6/68747470733a2f2f692e696d6775722e636f6d2f7675447455566a2e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/12693e8705166679a8d41c4989782f3038d53ab6/68747470733a2f2f692e696d6775722e636f6d2f7675447455566a2e706e67" alt="Example-RootPassEnter" data-canonical-src="https://i.imgur.com/vuDtUVj.png" /></a></li>
</ul>
<code>wget http://predatorcoin.online/setup/predatorcoin-install.sh</code>

<hr />

<em><strong>Step 8</strong></em>
<ul>
 	<li>Paste the code below into the Bitvise terminal then press enter</li>
</ul>
<code>bash predatorcoin-install.sh</code>

<a href="https://camo.githubusercontent.com/62a2a524ead43bd959bda3cec031a12a3022d659/68747470733a2f2f692e696d6775722e636f6d2f6d79766d4b54452e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/62a2a524ead43bd959bda3cec031a12a3022d659/68747470733a2f2f692e696d6775722e636f6d2f6d79766d4b54452e706e67" alt="Example-Bash" data-canonical-src="https://i.imgur.com/myvmKTE.png" /></a>

<hr />

<em><strong>Step 9</strong></em>
<ul>
 	<li>Sit back and wait for the install (this will take 10-20 mins)</li>
</ul>

<hr />

<em><strong>Step 10</strong></em>
<ul>
 	<li>When prompted to enter your GEN key - press enter</li>
</ul>
<a href="https://camo.githubusercontent.com/6a767f47fc47888dc7a0ee309c0a8e563bdc069c/68747470733a2f2f692e696d6775722e636f6d2f734c76576431532e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/6a767f47fc47888dc7a0ee309c0a8e563bdc069c/68747470733a2f2f692e696d6775722e636f6d2f734c76576431532e706e67" alt="Example-installing" data-canonical-src="https://i.imgur.com/sLvWd1S.png" /></a>

<hr />

<em><strong>Step 11</strong></em>
<ul>
 	<li>You will now see all of the relavant information for your server.</li>
 	<li>Keep this terminal open as we will need the info for the wallet setup. <a href="https://camo.githubusercontent.com/328898ca0f549fb8b6c3028cf1ff7c125cb3b83f/68747470733a2f2f692e696d6775722e636f6d2f5138374c636e572e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/328898ca0f549fb8b6c3028cf1ff7c125cb3b83f/68747470733a2f2f692e696d6775722e636f6d2f5138374c636e572e706e67" alt="Example-installing" data-canonical-src="https://i.imgur.com/Q87LcnW.png" /></a></li>
</ul>

<hr />

<h2><a id="user-content-section-d-preparing-the-local-wallet" class="anchor" href="https://github.com/STM0x0/Stim-1#section-d-preparing-the-local-wallet" aria-hidden="true"></a>Section D: Preparing the Local wallet</h2>
<em><strong>Step 1</strong></em>
<ul>
 	<li>Download and install the predatorcoin wallet <a href="https://github.com/predatorcoindev/predatorcoin/releases">here</a></li>
</ul>

<hr />

<em><strong>Step 2</strong></em>
<ul>
 	<li>Send EXACLY 5,000 predatorcoin to a receive address within your wallet.</li>
</ul>

<hr />

<em><strong>Step 3</strong></em>
<ul>
 	<li>Create a text document to temporarily store information that you will need.</li>
</ul>

<hr />

<em><strong>step 4</strong></em>
<ul>
 	<li>Go to the console within the wallet</li>
</ul>
<a href="https://camo.githubusercontent.com/5666e4613c4f87630ff8dd88f04d058b272464eb/68747470733a2f2f692e696d6775722e636f6d2f364e4d374739612e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/5666e4613c4f87630ff8dd88f04d058b272464eb/68747470733a2f2f692e696d6775722e636f6d2f364e4d374739612e706e67" alt="Example-console" data-canonical-src="https://i.imgur.com/6NM7G9a.png" /></a>

<hr />

<em><strong>Step 5</strong></em>
<ul>
 	<li>Type the command below and press enter</li>
</ul>
<code>masternode outputs</code>

<a href="https://camo.githubusercontent.com/711da3ac8f0c57f1cf46585ca6e26a9f77bf8f5b/68747470733a2f2f692e696d6775722e636f6d2f474437526f316d2e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/711da3ac8f0c57f1cf46585ca6e26a9f77bf8f5b/68747470733a2f2f692e696d6775722e636f6d2f474437526f316d2e706e67" alt="Example-outputs" data-canonical-src="https://i.imgur.com/GD7Ro1m.png" /></a>

<hr />

<em><strong>Step 6</strong></em>
<ul>
 	<li>Copy the long key (this is your transaction ID) and the 0 or 1 at the end (this is your output index)</li>
 	<li>Paste these into the text document you created earlier as you will need them in the next step.</li>
</ul>

<hr />

<h1><a id="user-content-section-e-connecting--starting-the-masternode" class="anchor" href="https://github.com/STM0x0/Stim-1#section-e-connecting--starting-the-masternode" aria-hidden="true"></a>Section E: Connecting &amp; Starting the masternode</h1>
<em><strong>Step 1</strong></em>
<ul>
 	<li>Go to the tools tab within the wallet and click open "masternode configuration file" <a href="https://camo.githubusercontent.com/014df9ca731eabc84ecb4af4274614351079b83d/68747470733a2f2f692e696d6775722e636f6d2f434f73667666412e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/014df9ca731eabc84ecb4af4274614351079b83d/68747470733a2f2f692e696d6775722e636f6d2f434f73667666412e706e67" alt="Example-create" data-canonical-src="https://i.imgur.com/COsfvfA.png" /></a></li>
</ul>

<hr />

<em><strong>Step 2</strong></em>
<ul>
 	<li>Fill in the form.</li>
 	<li>For <code>Alias</code> type something like "MN01" <strong>don't use spaces</strong></li>
 	<li>The <code>Address</code> is the IP and port of your server (this will be in the Bitvise terminal that you still have open).</li>
 	<li>The <code>PrivKey</code> is your masternode private key (This is also in the Bitvise terminal that you have open).</li>
 	<li>The <code>TxHash</code> is the transaction ID/long key that you copied to the text file.</li>
 	<li>The <code>Output Index</code> is the 0 or 1 that you copied to your text file. <a href="https://camo.githubusercontent.com/6c09d7ba48bfa343fe5de13df2072721ddec3ca5/68747470733a2f2f692e696d6775722e636f6d2f3962314933626b2e706e67" target="_blank" rel="noopener"><img src="https://camo.githubusercontent.com/6c09d7ba48bfa343fe5de13df2072721ddec3ca5/68747470733a2f2f692e696d6775722e636f6d2f3962314933626b2e706e67" alt="Example-create" data-canonical-src="https://i.imgur.com/9b1I3bk.png" /></a></li>
</ul>
<strong>Port:</strong> 8710

Click "File Save"

<hr />

<em><strong>Step 3</strong></em>
<ul>
 	<li style="list-style-type: none;">
<ul>
 	<li>Close out of the wallet and reopen Wallet *Click on the Masternodes tab "My masternodes"</li>
 	<li>Click start all in the masternodes tab</li>
</ul>
</li>
</ul>

<hr />

<em><strong>step 4</strong></em>
<ul>
 	<li>Check the status of your masternode within the VPS by using the command below:</li>
</ul>
<code>predatorcoin-cli masternode status</code>

<code>predatorcoin-cli getinfo</code>

*You should see <em><strong>status 9</strong></em>

If you do, congratulations! You have now setup a masternode. If you do not, please contact support and they will assist you.
