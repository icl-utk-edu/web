
Upload form
===========

<form class="needs-validation" novalidate="">
<label for="firstName" class="form-label">First name</label>
<input type="text" class="form-control" id="firstName" placeholder="" value="" required="">
<div class="invalid-feedback">Valid first name is required.</div>
<label for="lastName" class="form-label">Last name</label>
<input type="text" class="form-control" id="lastName" placeholder="" value="" required="">
<div class="invalid-feedback">Valid last name is required.</div>
<label for="email" class="form-label">Email</label>
<input type="email" class="form-control" id="email" placeholder="you@example.com" style="padding-right: 42px;" required="">
<div class="invalid-feedback">Please enter a valid email address for shipping updates.</div>
<label for="sitename" class="form-label">Site name</label>
<input type="text" class="form-control" id="sitename" placeholder="University of Education" required="">
<div class="invalid-feedback">Please enter a name of your installation site.</div>
<label for="segment" class="form-label">Segment</label>
<select class="form-select" id="segment" required="">
<option value="">Choose...</option>
<option>Academic</option>
<option>Classified</option>
<option>Government</option>
<option>Industry</option>
<option>Research</option>
<option>Vendor</option>
<option>Other</option>
</select>
<div class="invalid-feedback">Please select a valid segment.</div>
<label for="city" class="form-label">City</label>
<input type="text" class="form-control" id="city" required="">
<div class="invalid-feedback">Please enter a valid city.</div>
<label for="country" class="form-label">Country</label>
<input type="text" class="form-control" id="country" required="">
<div class="invalid-feedback">Please enter a valid country.</div>
<label for="sysname" class="form-label">System name</label>
<input type="text" class="form-control" id="sysname" placeholder="HPC Machine" required="">
<div class="invalid-feedback">Please enter a valid system name.</div>
<label for="integrator" class="form-label">Integrator</label>
<input type="text" class="form-control" id="integrator" required="">
<div class="invalid-feedback">Please enter a valid integrator.</div>
<label for="model" class="form-label">Computer model</label>
<input type="text" class="form-control" id="model">
<label for="processor" class="form-label">Processor name and model</label>
<input type="text" class="form-control" id="processor" placeholder="AMD EPYC 7742 or IBM POWER9 or Intel Xeon E5-2692v2." required="">
<div class="invalid-feedback">Please enter a valid processor name and model.</div>
<label for="procfreq" class="form-label">Processor frequency (GHz)</label>
<input type="text" class="form-control" id="procfreq" required="">
<div class="invalid-feedback">Please enter a valid processor frequency.</div>
<label for="proccores" class="form-label">Processor cores per socket</label>
<input type="text" class="form-control" id="proccores" required="">
<div class="invalid-feedback">Please enter a valid processor core count.</div>
<label for="sockets" class="form-label">Sockets per node</label>
<input type="text" class="form-control" id="sockets" required="">
<div class="invalid-feedback">Please enter a valid socket count.</div>
<label for="nodemem" class="form-label">Memory per node</label>
<input type="text" class="form-control" id="nodemem" required="">
<div class="invalid-feedback">Please enter a valid amount of memory per node.</div>
<label for="accelerator" class="form-label">Accelerator vendor and model</label>
<input type="text" class="form-control" id="accelerator" placeholder="AMD M100 or Intel Xeon Phi or NVIDIA V100 SXM2" required="">
<div class="invalid-feedback">Please enter a valid accelerator vendor and model.</div>
<label for="accelcores" class="form-label">Accelerator cores</label>
<input type="text" class="form-control" id="accelcores" required="">
<div class="invalid-feedback">Please enter a valid accelerator core count.</div>
<label for="accelcount" class="form-label">Accelerator per node</label>
<input type="text" class="form-control" id="accelcount" required="">
<div class="invalid-feedback">Please enter a valid accelerator count.</div>
<label for="interconnect" class="form-label">Interconnect vendor, model, connections</label>
<input type="text" class="form-control" id="interconnect" placeholder="Dell Gigabit 10G or Mellanox Infiniband QDR x4" required="">
<div class="invalid-feedback">Please enter a valid interconnect vendor and model.</div>
<label for="nodes" class="form-label">Node count</label>
<input type="text" class="form-control" id="nodes" required="">
<div class="invalid-feedback">Please enter a valid node count.</div>
<label for="hplaigflops" class="form-label">HPL-AI score (Giga-flop/s)</label>
<input type="text" class="form-control" id="hplaigflops" required="">
<div class="invalid-feedback">Please enter a valid HPL-AI score.</div>
<label for="hplaiimpl" class="form-label">HPL-AI implementation author and version</label>
<input type="text" class="form-control" id="hplaiimpl" required="">
<div class="invalid-feedback">Please enter a valid HPL-AI author and version.</div>
<label for="hplgflops" class="form-label">HPL score (Giga-flop/s) (in 64-bit floating-point arithmetic)</label>
<input type="text" class="form-control" id="hplgflops" required="">
<div class="invalid-feedback">Please enter a valid HPL score.</div>
<label for="outputFile" class="form-label">HPL-AI output file</label>
<input class="form-control" type="file" id="outputFile">
<label for="osname" class="form-label">Operating system</label>
<input type="text" class="form-control" id="osname">
<label for="compiler" class="form-label">Compiler</label>
<input type="text" class="form-control" id="compiler">
<label for="mathlib" class="form-label">Math libraries</label>
<input type="text" class="form-control" id="mathlib">
<label for="mpilib" class="form-label">MPI library</label>
<input type="text" class="form-control" id="mpilib">
<hr>
<button class="w-100 btn btn-primary btn-lg" type="submit">Submit</button>
</form>
