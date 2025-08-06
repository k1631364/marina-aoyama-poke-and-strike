---
layout: default
title: "Poke and Strike: Learning Task-Informed Exploration Policies"
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

# Poke and Strike: Learning Task-Informed Exploration Policies

<a href="https://scholar.google.com/citations?user=OJmSDo8AAAAJ&hl=ja&oi=ao" target="_blank" style="color: #5faee3; text-decoration: none;">Marina Y. Aoyama</a><sup>1</sup>, 
<a href="https://scholar.google.co.jp/citations?user=1L5kTRcAAAAJ&hl=en&oi=sra" target="_blank" style="color: #5faee3; text-decoration: none;">Joao Moura</a><sup>1</sup>, 
<span style="color: #5faee3; text-decoration: none;">Juan Del Aguila Ferrandis</span><sup>1</sup>
<a href="https://scholar.google.com/citations?user=JdRs1sQAAAAJ&hl=ja&oi=ao" target="_blank" style="color: #5faee3; text-decoration: none;">Sethu Vijayakumar</a><sup>1</sup>, 

<sup>1</sup>The University of Edinburgh

Conference on Robot Learning (CoRL) 2025 

<div class="button-container">
  <a href="https://ieeexplore.ieee.org/abstract/document/11053701" target="_blank" class="my-button">
    <span class="icon"><i class="fas fa-file-alt"></i></span>
    <span>Paper</span>
  </a>
  
  <a href="#" id="jumpToVideo" class="my-button">
    <span class="icon"><i class="fas fa-video"></i></span>
    <span>Video</span>
  </a>
</div>

Our approach learns to explore physical properties that matter for the task! 

<video width="800" height="450" controls muted loop autoplay playsinline webkit-playsinline>
  <source src="videos/3min_video_poke_and_strike.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

## Abstract 
In many dynamic robotic tasks, such as striking pucks into a goal outside the reachable workspace, the robot must first identify the relevant physical properties of the object for successful task execution, as it is unable to recover from failure or retry without human intervention. To address this challenge, we propose a task-informed exploration approach, based on reinforcement learning, that trains an exploration policy using rewards automatically generated from the sensitivity of a privileged task policy to errors in estimated properties. We also introduce an uncertainty-based mechanism to determine when to transition from exploration to task execution, ensuring sufficient property estimation accuracy with minimal exploration time. Our method achieves a 90% success rate on the striking task with an average exploration time under 1.2 seconds—significantly outperforming baselines that achieve at most 40% success or require inefficient querying and retraining in a simulator at test time. Additionally, we demonstrate that our task-informed rewards capture the relative importance of physical properties in both the striking task and the classical CartPole example. Finally, we validate our approach by demonstrating its ability to identify object properties and adjust task execution in a physical setup using the KUKA iiwa robot arm. 

## Summary Video (with voice 🔈) 
<video id="myVideo" width="800" height="450" controls loop>
  <source src="videos/3min_video_poke_and_strike.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

## Method

We propose a task-informed exploration approach, based on reinforcement learning, that trains an exploration policy using rewards automatically generated from the sensitivity of a privileged task policy to errors in estimated properties. We also introduce an uncertainty-based mechanism to determine when to transition from exploration to task execution, ensuring sufficient property estimation accuracy with minimal exploration time. 

<video width="800" height="450" controls muted loop autoplay playsinline webkit-playsinline>
  <source src="videos/method_nosound.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

## Results 
All videos are shown at 1.0× speed!

### Four surface following tasks 

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 2rem 1rem; max-width: 900px; margin: auto;">

  <div style="text-align: center;">
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="assets/videos/smallbrush_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Small brush</div>
  </div>

  <div style="text-align: center;">
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="assets/videos/widebrush_short_compressed_noaudio.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Wide brush</div>
  </div>

  <div style="text-align: center;">
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="assets/videos/broom_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Broom</div>
  </div>

  <div style="text-align: center;">
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="assets/videos/sponge_short_compressed_noaudio.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Sponge</div>
  </div>

</div>

### Online adaptation 

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 1rem; max-width: 900px; margin: auto;">

  <div style="text-align: center;">
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="assets/videos/real_online_inclination_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Changing inclination</div>
  </div>

  <div style="text-align: center;">
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="assets/videos/real_online_deformable_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Deformable surface</div>
  </div>

</div>

<div style="display: flex; justify-content: center; gap: 1rem; max-width: 800px; margin: 2rem auto 0 auto;">

  <div style="text-align: center;">
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="assets/videos/smallbrush_step_short_compressed_noaudio.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Step painting</div>
  </div>

</div>


### Demo only (baseline) vs. Pre-train+Demo (proposed) 

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 1rem; max-width: 900px; margin: auto;">

  <div style="text-align: center;">
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="videos/striking_estimates_nosound.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Demo only (baseline)<br>Pressing too much! Tool slippage. </div>
  </div>

  <div style="text-align: center;">
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="videos/egg_estimates_nosound.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Pre-train+Demo (proposed) </div>
  </div>

</div>

### Robustness to external disturbances 

<div style="display: flex; justify-content: center; gap: 1rem; max-width: 800px; margin: auto;">
  
  <div style="text-align: center;">
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="assets/videos/real_disturbances_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <!--<div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Real</div>-->
  </div>

</div>

### Citation 
<div class="citation-wide">
  <div style="position: relative; max-width: 950px; margin: 0 auto;">
    <button onclick="copyBibtex(this)" style="
      position: absolute;
      top: 0.5rem;
      right: 0.5rem;
      font-size: 0.75rem;
      padding: 0.3rem 0.6rem;
      border: none;
      background: #ddd;
      border-radius: 4px;
      cursor: pointer;
      z-index: 1;
    ">Copy</button>
    <pre style="
      font-family: monospace;
      font-size: 0.85rem;
      background: #f5f5f5;
      border: 1px solid #ccc;
      border-radius: 6px;
      padding: 2rem 0.75rem 0.75rem 0.75rem;  /* extra top padding for the button */
      overflow-x: auto;
      white-space: pre-wrap;
      word-break: break-word;
    "><code id="bibtex-block">@article{aoyama2025few,
  title={Few-shot transfer of tool-use skills using human demonstrations with proximity and tactile sensing},
  author={Aoyama, Marina Y and Vijayakumar, Sethu and Narita, Tetsuya},
  journal={IEEE Robotics and Automation Letters},
  year={2025},
  publisher={IEEE}
}</code></pre>
  </div>
</div>

<script>
  function copyBibtex(button) {
    const code = button.nextElementSibling.querySelector('code');
    navigator.clipboard.writeText(code.textContent).then(() => {
      button.textContent = 'Copied!';
      setTimeout(() => { button.textContent = 'Copy'; }, 2000);
    });
  }
</script>



