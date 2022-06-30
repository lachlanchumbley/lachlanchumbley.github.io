# Supermarket Object Dataset
## Welcome to the Coles Supermarket Object Dataset

The dataset consists of 3D water-tight mesh models of 50 supermarket objects


The objects were picked from 10 different categories:
- Small Box (Food)
- Large Box (Food)
- Regular Cylinder (Food)
- Irregular Cylinder (Food)
- Small Box
- Large Box
- Regular Cylinder
- Irregular Cylinder
- Packet
- Irregular Shapes

The dataset was created to assist in the development of data-driven robotic grasping approaches.

You can down the dataset [**here**](https://github.com/lachlanchumbley/lachlanchumbley.github.io/edit/main/index.md).

## The objects


<div float="left" style="display: flex; flex-direction: row; flex-wrap: wrap;">
  {% for image in site.static_files %}
      {% if image.path contains 'images' %}
        {% if image.path contains '.png' %}
            {% assign pathsplit = image.path | split: "/" %}
            {% assign length = pathParts.size | minus: 1 %}
            {% assign filesplit = pathsplit[length] | split: "." %}
            <!-- ten percent for ten per row?? -->
            <div style="width: 10%; min-width: 250px;">
              <!-- <strong>Object Name:</strong> {{ filesplit[0] }}  -->
              {{ filesplit[0] }}
              <img src="{{ site.baseurl }}{{ image.path }}" alt="image" width="80%"/>
            </div>
        {% endif %}
      {% endif %}
  {% endfor %}
</div>
