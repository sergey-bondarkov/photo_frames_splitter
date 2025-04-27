# Film scans splitter
This algorithm 
- takes in all TIF files put in `input` directory, 
- converts them to temporary smaller JPGs,
- applies a list of transformations to find places of sharp vertical intensity change,
- finds clusters of such edges with DBSCAN and averages their x values,
- splits the original image at the scaled X (proportional to the original resize),
- saves thus obtained individual frames as TIF and JPG,
- removes temporary JPGs.

Should work one any film strip but may require tuning some transformations parameters.
