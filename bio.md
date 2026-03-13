---
layout: page
title: D-BORA — les biographies
last_modified_at: 2024-12-04
---

<section id="members">
    <div class="row row-cols-1 row-cols-md-2 g-5">
        <div class="col">
            <div class="bio-card text-center">
                <img class="rounded-circle member-photo" src="assets/img/jp.jpg" width="200" height="200" alt="Jean-Pierre" />
                <h2 class="display-4 mt-3 mb-0">JP</h2>
                <p class="member-role">Chant, guitare rythmique, harmonica</p>
                <div class="bio-text text-start">
                    {% capture my_include %}{% include jp_bio.md %}{% endcapture %}
                    {{ my_include | markdownify }}
                </div>
            </div>
        </div>
        <div class="col">
            <div class="bio-card text-center">
                <img class="rounded-circle member-photo" src="assets/img/fred.jpg" width="200" height="200" alt="Frédéric" />
                <h2 class="display-4 mt-3 mb-0">Fred</h2>
                <p class="member-role">Guitare solo</p>
                <div class="bio-text text-start">
                    {% capture my_include %}{% include fred_bio.md %}{% endcapture %}
                    {{ my_include | markdownify }}
                </div>
            </div>
        </div>
        <div class="col">
            <div class="bio-card text-center">
                <img class="rounded-circle member-photo" src="assets/img/math.jpg" width="200" height="200" alt="Mathieu" />
                <h2 class="display-4 mt-3 mb-0">Math</h2>
                <p class="member-role">Batterie et chœurs</p>
                <div class="bio-text text-start">
                    {% capture my_include %}{% include math_bio.md %}{% endcapture %}
                    {{ my_include | markdownify }}
                </div>
            </div>
        </div>
        <div class="col">
            <div class="bio-card text-center">
                <img class="rounded-circle member-photo" src="assets/img/bob.jpg" width="200" height="200" alt="Robert" />
                <h2 class="display-4 mt-3 mb-0">Bob</h2>
                <p class="member-role">Guitare basse et chœurs</p>
                <div class="bio-text text-start">
                    {% capture my_include %}{% include bob_bio.md %}{% endcapture %}
                    {{ my_include | markdownify }}
                </div>
            </div>
        </div>
    </div>
    <div class="tribute text-center">
        <img class="rounded-circle member-photo" src="assets/img/deborah.jpg" width="250" height="250" alt="Déborah" />
        <h2 class="display-4 fst-italic mt-3">Déborah</h2>
    </div>
</section>
