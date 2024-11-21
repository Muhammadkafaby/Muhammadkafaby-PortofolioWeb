<script>
export default {
  data() {
    return {
      activeTab: 1,
      tech: [
        {
          id: 1,
          name: "Python",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/112/PNG/512/python_18894.png",
          status: "Advanced",
        },
        {
          id: 2,
          name: "YML",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2107/PNG/512/file_type_light_yaml_icon_130421.png",
          status: "Advanced",
        },
        {
          id: 3,
          name: "PHP",
          imageUrl:
            "https://cdn.iconscout.com/icon/free/png-256/free-php-2038871-1720084.png",
          status: "Advanced",
        },
        {
          id: 4,
          name: "Javascript",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2415/PNG/512/javascript_original_logo_icon_146455.png",
          status: "Advance",
        },
        {
          id: 5,
          name: "Laravel",
          imageUrl: "https://cdn.worldvectorlogo.com/logos/laravel-2.svg",
          status: "Advance",
        },
        {
          id: 6,
          name: "Codeigniter",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2415/PNG/512/codeigniter_plain_wordmark_logo_icon_146592.png",
          status: "Intermediate",
        },
        {
          id: 7,
          name: "Java",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2699/PNG/512/java_src_logo_icon_170556.png",
          status: "Intermediate",
        },
        {
          id: 8,
          name: ".Net",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2415/PNG/512/dot_net_plain_wordmark_logo_icon_146545.png",
          status: "Beginner",
        },
        {
          id: 9,
          name: "NodeJS",
          imageUrl:
            "https://cdn.iconscout.com/icon/free/png-256/free-node-js-1174925.png",
          status: "Advance",
        },
        {
          id: 10,
          name: "Tailwind",
          imageUrl:
            "https://upload.wikimedia.org/wikipedia/commons/d/d5/Tailwind_CSS_Logo.svg",
          status: "Beginner",
        },
        {
          id: 11,
          name: "Bootstrap",
          imageUrl:
            "https://getbootstrap.com/docs/5.2/assets/brand/bootstrap-logo-shadow.png",
          status: "Intermediate",
        },
        {
          id: 12,
          name: "Shell",
          imageUrl:
            "https://cdn2.iconfinder.com/data/icons/file-type-46/512/Bash_shell_script-1024.png",
          status: "Advance",
        },
      ],
      tools: [
        {
          id: 1,
          name: "Git",
          imageUrl:
            "https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png",
          status: "Version Control",
        },
        {
          id: 2,
          name: "GitHub",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2429/PNG/512/github_logo_icon_147285.png",
          status: "Git Hosting",
        },
        {
          id: 5,
          name: "GitLab",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2415/PNG/512/gitlab_original_logo_icon_146503.png",
          status: "GitLab Hosting",
        },
        {
          id: 3,
          name: "MongoDB",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2415/PNG/512/mongodb_plain_wordmark_logo_icon_146423.png",
          status: "Database",
        },
        {
          id: 4,
          name: "MySQL",
          imageUrl: "https://cdn-icons-png.flaticon.com/512/5968/5968313.png",
          status: "Database",
        },
        {
          id: 13,
          name: "PostgreSQL",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2415/PNG/512/postgresql_plain_wordmark_logo_icon_146390.png",
          status: "Database",
        },
        {
          id: 6,
          name: "Docker",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2415/PNG/512/docker_original_wordmark_logo_icon_146557.png",
          status: "Containerization",
        },
        {
          id: 7,
          name: "Kubernetes",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2699/PNG/512/kubernetes_logo_icon_168359.png",
          status: "Container Orchestration",
        },
        {
          id: 8,
          name: "Jenkins",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2699/PNG/512/jenkins_logo_icon_170552.png",
          status: "CI/CD",
        },
        {
          id: 9,
          name: "Elasticsearch",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2107/PNG/512/file_type_elastic_icon_130625.png",
          status: "Monitoring",
        },
        {
          id: 10,
          name: "Kibana",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2699/PNG/512/elasticco_kibana_logo_icon_168223.png",
          status: "Monitoring",
        },
        {
          id: 11,
          name: "Logstash",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2699/PNG/512/elasticco_logstash_logo_icon_171187.png",
          status: "Monitoring",
        },
        {
          id: 12,
          name: "Metricbeat",
          imageUrl:
            "https://seeklogo.com/images/E/elastic-beats-logo-02512BDFD2-seeklogo.com.png",
          status: "Monitoring",
        },
        {
          id: 14,
          name: "Linux",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2235/PNG/512/linux_os_logo_icon_134670.png",
          status: "Operating System",
        },
        {
          id: 15,
          name: "Ubuntu",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2415/PNG/512/ubuntu_plain_wordmark_logo_icon_146632.png",
          status: "Operating System",
        },
      ],
    };
  },
};
</script>
<template>
  <div
    class="bg-[#1e1e1f] px-5 py-5 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-amber-50 mx-3 mb-5"
  >
    <article data-page="about">
      <header>
        <div
          class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center"
        >
          About Me &nbsp;
          <div
            class="h-[1px] w-32 bg-amber-200 md:w-96 aos-init aos-animate"
            data-aos="zoom-in-left"
            data-aos-duration="600"
          ></div>
        </div>
      </header>

      <section
        class="text-sm md:text-lg text-justify flex flex-col gap-4 md:flex-row md:gap-8 md:justify-left md:items-center"
      >
        <div class="flex justify-center">
          <img
            class="w-9/12 rounded-full mb-3 fadein-up"
            src="https://media.istockphoto.com/vectors/spy-icon-with-binary-code-vector-id824577262?k=6&m=824577262&s=170667a&w=0&h=75MEzeQqAauy_FE1v44t_tF6RMeRyCcitbYDsl-flXo="
            alt="Foto"
          />
        </div>
        <div class="md:w-7/12">
          <p class="mb-3 md:mb-7 fadein-left fadeins-1">
            &nbsp; &nbsp; &nbsp; Hi everyone! My name is Muhammad Kafaby, and
            I’m a DevOps Engineer from Indramayu, West Java. With 2 years of
            experience in the field, I am deeply passionate about what I do. For
            me, building CI/CD pipelines and implementing security programs
            isn’t just about technical work—it’s an art form that combines
            precision, creativity, and aesthetic value.
          </p>
          <p class="mb-3 fadein-left fadeins-2">
            &nbsp; &nbsp; &nbsp; My role is to ensure that your systems are
            efficient, secure, and reliable, while also maintaining a seamless
            workflow to support your development processes. I specialize in
            creating scalable and automated solutions that empower teams to
            deliver software faster and more securely. If you're looking for
            someone to help optimize your systems or build innovative DevOps
            solutions, feel free to reach out. Let’s collaborate to bring your
            vision to life!
          </p>
        </div>
      </section>
    </article>
  </div>

  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div
          class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center"
        >
          <div
            class="h-[1px] w-10 bg-amber-200 md:w-20 aos-init aos-animate"
            data-aos="zoom-in-left"
            data-aos-duration="600"
          ></div>
          &nbsp; Skills
        </div>
      </header>
      <section>
        <div>
          <ul
            class="flex flex-wrap text-sm font-medium text-center text-gray-500 dark:text-gray-400 mb-5"
          >
            <li class="mr-2">
                            <button
                class="inline-block px-4 py-3 rounded-lg"
                :class="{
                  'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 1,
                }"
                @click="activeTab = 1"
              >
                Tech Stack
              </button>
              </li>
              <li class="mr-2">
                <button
                  class="inline-block px-4 py-3 rounded-lg"
                  :class="{
                    'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 2,
                  }"
                  @click="activeTab = 2"
                >
                  Tools
                </button>
            </li>
          </ul>
        </div>
        <div v-show="activeTab === 1">
          <div
            class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12"
          >
            <div v-for="item in tech" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-amber-200 px-2 py-2 hover:bg-amber-200 hover:bg-opacity-10 md:gap-3 lg:px-3"
              >
                <div
                  class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in"
                >
                  <img
                    alt="HTML"
                    loading="lazy"
                    width="32"
                    height="32"
                    decoding="async"
                    data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]"
                    :src="item.imageUrl"
                    style="color: transparent"
                  />
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div
                    class="tech font-medium text-secondary transition-all duration-300 translate-y-0"
                  >
                    {{ item.name }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-amber-200 transition-all duration-300 md:text-xs lg:text-sm"
                  >
                    {{ item.status }}
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div v-show="activeTab === 2">
          <div
            class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12"
          >
            <div v-for="item in tools" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-amber-200 px-2 py-2 hover:bg-amber-200 hover:bg-opacity-10 md:gap-3 lg:px-3"
              >
                <div
                  class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in"
                >
                  <img
                    alt="HTML"
                    loading="lazy"
                    width="32"
                    height="32"
                    decoding="async"
                    data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]"
                    :src="item.imageUrl"
                    style="color: transparent"
                  />
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div
                    class="tech font-medium text-secondary transition-all duration-300 translate-y-0"
                  >
                    {{ item.name }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-amber-200 transition-all duration-300 md:text-xs lg:text-sm"
                  >
                    {{ item.status }}
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style>
.fadein-left {
  opacity: 0;
  animation: fadeInLeft 0.5s ease-out forwards;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(100%);
  }

  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadeins-1 {
  animation-delay: 500ms;
}

.fadeins-2 {
  animation-delay: 800ms;
}

.img-tech,
.tech {
  transition: transform 0.3s ease;
}

.item-tech:hover .img-tech {
  transform: scale(1.3);
}

.item-tech:hover .tech {
  transform: translateY(-12px);
}

.item-tech:hover .status-tech {
  opacity: 1;
}

/* Hacker theme colors */
body {
  background-color: #0f0f0f;
  color: #00ff00;
}

.text-amber-50 {
  color: #00ff00;
}

.text-white {
  color: #00ff00;
}

.bg-amber-200 {
  background-color: #003500;
}

.text-amber-200 {
  color: #00ff00;
}

.border-amber-200 {
  border-color: #00ff00;
}

/* .hover\:bg-amber-200:hover {
  background-color: #00ff00;
} */

.hover\:text-white:hover {
  color: #00ff00;
}
</style>
