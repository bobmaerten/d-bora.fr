---
layout: page
title: D-BORA — les biographies
last_modified_at: 2024-12-04
---

<section id="members">
    <div class="accordion accordion-flush" id="accordionBio">
        <div class="row row-cols-1 row-cols-md-2 row-cols-lg-4 g-5 text-center">
            <div class="col">
                <img
                    class="rounded-circle"
                    src="assets/img/jp.jpg"
                    width="250"
                    height="250"
                    alt="Jean-Pierre"
                />
                <div class="mt-3">
                    <p class="text-center">Guitare rythmique et chant</p>
                    <div class="accordion-item">
                        <h2 class="accordion-header" id="headingJP">
                            <button
                                class="accordion-button collapsed"
                                type="button"
                                data-bs-toggle="collapse"
                                data-bs-target="#collapseJP"
                                aria-expanded="false"
                                aria-controls="collapseJP"
                            >
                                <span
                                    class="display-4 d-block w-100 text-center"
                                    >JP</span
                                >
                            </button>
                        </h2>
                    </div>
                    <div
                        id="collapseJP"
                        class="accordion-collapse collapse"
                        aria-labelledby="headingJP"
                        data-bs-parent="#accordionBio"
                    >
                        <div class="accordion-body">
                            {% capture my_include %}{% include jp_bio.md %}{% endcapture
                            %} {{ my_include | markdownify }}
                        </div>
                    </div>
                </div>
              </div>
            <div class="col">
                <img
                    class="rounded-circle"
                    src="assets/img/fred.jpg"
                    width="250"
                    height="250"
                    alt="Frédéric"
                />
                <div class="mt-3">
                    <p class="text-center">Guitare solo</p>
                    <div class="accordion-item">
                        <h2 class="accordion-header" id="headingFred">
                            <button
                                class="accordion-button collapsed"
                                type="button"
                                data-bs-toggle="collapse"
                                data-bs-target="#collapseFred"
                                aria-expanded="false"
                                aria-controls="collapseFred"
                            >
                                <span
                                    class="display-4 d-block w-100 text-center"
                                    >Fred</span
                                >
                            </button>
                        </h2>
                    </div>
                    <div
                        id="collapseFred"
                        class="accordion-collapse collapse"
                        aria-labelledby="headingFred"
                        data-bs-parent="#accordionBio"
                    >
                        <div class="accordion-body">
                            {% capture my_include %}{% include fred_bio.md %}{%
                            endcapture %} {{ my_include | markdownify }}
                        </div>
                    </div>
                </div>
              </div>
            <div class="col">
                <img
                    class="rounded-circle"
                    src="assets/img/math.jpg"
                    width="250"
                    height="250"
                    alt="Mathieu"
                />
                <div class="mt-3">
                    <p class="text-center">Batterie</p>
                    <div class="accordion-item">
                        <h2 class="accordion-header" id="headingMath">
                            <button
                                class="accordion-button collapsed"
                                type="button"
                                data-bs-toggle="collapse"
                                data-bs-target="#collapseMath"
                                aria-expanded="false"
                                aria-controls="collapseMath"
                            >
                                <span
                                    class="display-4 d-block w-100 text-center"
                                    >Math</span
                                >
                            </button>
                        </h2>
                    </div>
                    <div
                        id="collapseMath"
                        class="accordion-collapse collapse"
                        aria-labelledby="headingMath"
                        data-bs-parent="#accordionBio"
                    >
                        <div class="accordion-body">
                            {% capture my_include %}{% include math_bio.md
                            %}{% endcapture %} {{ my_include | markdownify
                            }}
                        </div>
                    </div>
                    <div
                        id="collapseMath"
                        class="accordion-collapse collapse"
                        aria-labelledby="headingMath"
                        data-bs-parent="#accordionBio"
                    >
                        <div class="accordion-body">
                            {% capture my_include %}{% include math_bio.md %}{%
                            endcapture %} {{ my_include | markdownify }}
                        </div>
                    </div>
                </div>
              </div>
            <div class="col">
                <img
                    class="rounded-circle"
                    src="assets/img/bob.jpg"
                    width="250"
                    height="250"
                    alt="Robert"
                />
                <div class="mt-3">
                    <p class="text-center">Guitare basse et chœurs</p>
                    <div class="accordion-item">
                        <h2 class="accordion-header" id="headingBob">
                            <button
                                class="accordion-button collapsed"
                                type="button"
                                data-bs-toggle="collapse"
                                data-bs-target="#collapseBob"
                                aria-expanded="false"
                                aria-controls="collapseBob"
                            >
                                <span
                                    class="display-4 d-block w-100 text-center"
                                    >Bob</span
                                >
                            </button>
                        </h2>
                    </div>
                    <div
                        id="collapseBob"
                        class="accordion-collapse collapse"
                        aria-labelledby="headingBob"
                        data-bs-parent="#accordionBio"
                    >
                        <div class="accordion-body">
                            {% capture my_include %}{% include bob_bio.md
                            %}{% endcapture %} {{ my_include | markdownify
                            }}
                        </div>
                    </div>
                 </div>
            </div>
        </div>
    </div>
    <div class="py-5 text-center">
        <img
            class="rounded-circle"
            src="assets/img/deborah.jpg"
            width="250"
            height="250"
            alt="Déborah"
        />
        <h2 class="display-4 fst-italic">Déborah</h2>
    </div>
</section>
