# Houdini


# Set ENV VAR for Job

"C:\Users\damia\OneDrive\Documents\houdini20.5\houdini.env"

add

HOU_PRINT_JOB = "C:\Users\damia\Projects\Katana_One_Drive\OneDrive - TCG International\Projects\Houdini_Print"


# ADD ENV to file browser

"C:\Users\damia\OneDrive\Documents\houdini20.5\jump.pref"

Add 

"$HOU_PRINT_JOB"


# Channel reference in Materialx

create null

customozie param interface, add string or color

copy parameter

paste relative refernce into color or file path

"$HOU_PRINT_JOB/Assets/Pathfinder/asset/textures/int/`chs("../tex/texture_name")`/`chs("../tex/texture_name")`_BaseColor.png"

refernces the node "txt" with prefix for the texturename "texture_name"

or 

ch("../../Common_Colors/Blackr")

ch("../../Common_Colors/Blackg")

ch("../../Common_Colors/Blackb")

refernces a node "Common_Colors" with a color "Black" then the r,g,b commpents into another color. 

# Break up UV's with noise

mtlxtexcoord1   ------------------------ mtlx add ---> texcords
                -> mtlxunifiednoise2ds

sample the uvs of the object, then add noise to them to break up repeating textures.

https://www.youtube.com/watch?v=ZRUbg6gYguA&t=254s


# PBR black

the diffuse black pbr value is .013 in srb linear, or 30 in 0-255. 


# Select by Material

Right Click on Material in hiearchy and "Select all bound geometry"

# Reset the hiearchy

right click on the root and "Clear Overrides on this branch" 