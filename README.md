--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#programme de NaomiK , FluoroPolymers™

- Feel free to alter the variables to make different simulations . Think of it as a simulation engine more than a finished product 
- You will need NumPy to run this
- Should save both .png files in the root folder 
- deleting __pycache__ is no problem , actually you should clear it at some point if you run too many simulations . I didnt make them overwrite previous cache files .
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Sphere Demo : 

<img width="2100" height="1260" alt="Image" src="https://github.com/user-attachments/assets/b8ab2d22-9b1f-4f12-943c-8535cba3d098" /># Ricci-Flow-Simulation

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Flattened DEmo :

<img width="2100" height="1260" alt="Image" src="https://github.com/user-attachments/assets/cf984fef-7d2d-4ec4-8817-8bf9fd2a8729" />

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

This program implements the discrete curvaure flow on a 2D triangulated surface mesh to flatten or uniformize its geometry *(discrete analogue to the Ricci Flow that proved the Poincaré Conjecture)*

**-Underlying Principle** : Every vertex has a discrete Gaussian Curvature


$$
K_i = 2\pi - \sum_{j \ne i} \theta_j^{ik}
$$

Where $\theta^{jk}_i$ is the interior angle at vertex $i$ in triangle $\triangle Δijk$ . Under Ricci Flow , circle packings or conformal edge factors evovle dynamically so $K_i \rightarrow 0$ (or constant curvature)*
-The Challenge : Dynamically adjust vertex coordinates or conformal metric scaling factors $ui$ at each step :

$$
\frac{du_i}{dt} = -K_i
$$

This program updates the triangulation geometry using iterative matrix solvers (such as cnjugate gradient) while avoiding inverted triangles
I also mapped an arbitrary 3D genus-0 mesh into a conformal , minimal-distortion sphere
