<script lang='ts' context='module'>
	export const prerender = true;
</script>

<script lang='ts'>
	import a2d from '../../../assets/graphics/Analog2Digital.svg';
</script>

<svelte:head>
	<title>E&sup2;G | Background Info</title>
</svelte:head>

<div class='content'>
	<div class='title'>Background Info</div>

	<div class='section'>
		<h1 class='section__title'>What is EEG</h1>
		<p>
			Electroencephalography or EEG henceforth, is a method of measuring brain activity. It works by
			measuring the voltage between two points on the skull, typically using electrodes, probes
			henceforth. This is the technology that you might recognize from the sci-fi brain to computer
			interfaces or from a sleep lab. This fundamentally works by picking up on the electrical signals
			from different parts of your brain which can be used to determine the rough state of that area
			of the brain.
		</p>
	</div>

	<div class='section'>
		<h1 class='section__title'>Analog and Digital Converters</h1>
		<div class='section__content'>
			<img src={a2d} alt='Analog to digital conversion'>
			<p>
				One major component of EEG is the process of converting the analog data captured by the probes
				into digital signals that can be handled by the brain. Computers work using a binary system to
				represent data, high voltage or low voltage, the voltage points are discrete. The values
				coming from the brain are continuous. Therefore, some process must occur to turn analog
				voltage levels into digital values. These devices can be found in many different products,
				including but not limited to: Modern Voltmeters, Oscilloscopes, and Digital Cameras. We will
				call these converters A->D for shorthand. An everyday example of this is the old AM (Analog)
				vs the newer FM (Digital) Radios, you might have noticed that AM gets more noisy and quieter
				as you get further from the station (In this case, the Brain), while FM stays just as clear
				and loud as long as it plays.
			</p>
		</div>

		<div class='section--sub'>
			<h1 class='section--sub__title'>Why those converters are so expensive</h1>
			<div class='section__content'>
				<p>
					Analog to Digital converters aren't actually hugely expensive, but the ones used for EEG are
					very expensive for a number of reasons:
				</p>
				<ul class='list-disc'>
					<li>In the Industry Standard configuration, they have to work at very low voltages</li>
					<li>Crosstalk can occur simply by having other wires to the signal</li>
					<li>
						Involves quantization of the input, so it necessarily introduces a small amount of error
						or noise, which takes good engineering to fix
					</li>
				</ul>
			</div>
		</div>

		<div class='section'>
			<h1 class='section__title'>
				Electronic component reference
			</h1>

			<div class='section__content'>
				<table>
					<tr>
						<th>Component</th>
						<th>Description</th>
					</tr>
					<tr>
						<td>Multiplexer<br>(HW-178)</td>
						<td>Analog switch that connects one input selected from several inputs to a single output.</td>
					</tr>
					<tr>
						<td>Instrumental Amplifier<br>(AD620)</td>
						<td>Boosts the EEG signals up so they are more noise tolerant (because the signal is more powerful)</td>
					</tr>
					<tr>
						<td>Microcontroller<br>(Arduino Due)</td>
						<td>Relatively expensive single-board computer that can run code and output faster than most others
							available.
						</td>
					</tr>
					<tr>
						<td>Microcontroller<br>(ESP8266)</td>
						<td>Relatively cheap single-board computer that runs very fast, but with limited output options.</td>
					</tr>
				</table>
			</div>
		</div>
	</div>
</div>

<style lang='scss'>
  @use "../../../assets/style/poster-content" with (
  $color: var(--red),
);
</style>
