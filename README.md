# InsightAccess


# Goals

* Build an AI that can **answer questions and make useful predictions** about current and future water availability in CDMX.
* Build a UX that’s sufficiently **accessible for low-tech users** (DroughtPredictorGPT?)
* Automate and streamline the data sourcing and analysis pipeline to support an **open sourced project community**.
* Generalize the pipeline/tool to be useful for other research (eg food shortages, travel issues, public safety, etc)
* Structure the outputs to be **digestible for GPTs**, eventually personal assistants, etc. 

# Plan

1. **Define Key Questions**

   * Where and when will there be water shortages in CDMX in the next 6 months? 
      * Begin with shorter timeframes and gradually expand the scope.
   * How does upcoming water availability compare to historical averages for specific locations (zip code/address)?
   * What are rainfall patterns (by month/year) and how do they affect water availability?
   * What are government initiatives to address the water shortage?
   * How are candidates in the upcoming election addressing the water crisis?
   * Are there tax breaks for water conservation, and how can citizens access them?

2. **Identify Data Sources**

   * **Rainfall by weather station:** https://datos.gob.mx/busca/dataset/precipitacion-actual-y-acumulada-por-estacion
   * **Agua en tu colonia: [invalid URL removed]:** Indicates water sources for specific neighborhoods 
   * **Research paper APIs:**
      * Crossref API  
      * arXiv API 
      * PubMed API
      * CORE API
   * **Monthly average rainfall statistics by state:** https://smn.conagua.gob.mx/es/climatologia/temperaturas-y-lluvias/resumenes-mensuales-de-temperaturas-y-lluvias
   * **API Get Catalog gob.mx (requires token):** https://datos.gob.mx/blog/csmn.conagua.gob.mxatalogo-apidatosgobmx?category=api-cdn&tag=nula 
   * **Social media scraping:** Track mentions of water outages
   * **Government records:** Document any tax breaks related to the water shortage
   * **Citizen science initiatives:** Explore potential collaborations
   * **Global weather data:** https://weatherspark.com/ 
   * **Water Consumption (last updated June 2023):** https://datos.cdmx.gob.mx/dataset/consumo-agua
   * **Water incidents 2022-2023:** https://datos.cdmx.gob.mx/dataset/reportes-de-agua/resource/a8069e94-c7cb-45d7-8166-561e80884422
   * **Climate/weather forecasts**
   * **INEGI - fuente de agua potable:** https://cuentame.inegi.org.mx/territorio/agua/dispon.aspx?tema=T
   * **Sistema de Informacion Hidrologica:** https://sih.conagua.gob.mx/
   * **Geographical information:** https://api.copomex.com/documentacion/inicio
   * **Clean Water AI (Microsoft project):** Investigate potential use cases
   * **Government announcements:**  https://data.consejeria.cdmx.gob.mx/index.php/gaceta#ver-indice (shows PDF links - no API present)

3. **Explore Existing Frameworks/Tools**

   * **Perigon: https://www.goperigon.com/:** Aggregates and distills news sources - API available
   * **Haystack: https://haystack.deepset.ai/ (Github: https://github.com/deepset-ai/haystack):** Semantic search for large datasets
   * **Langchain:** Open-source AI tool with broad applications.

4. **Evaluation Metrics**  

   * **Define "effective":** The tool should accurately answer questions and predict current and future water availability in CDMX. 
   * **Benchmarking:** Compare performance to similar tools (e.g., Perplexity: https://www.perplexity.ai/search/Where-and-when-W.aXQ7CuScCAx_BINheYKQ?s=u).

5. **Sample Articles**

   * https://www.milenio.com/opinion/ricardo-raphael/politica-zoom/la-guerra-del-agua-ya-comenzo
   * https://wradio.com.mx/2024/01/26/sacmex-deja-con-recorte-de-agua-a-284-colonias-de-la-cdmx/


## Water Availability Data Points

* **Reservoirs**
    * % Full
    * Liters remaining
    * Zonal distribution of water

* **Pozos (Wells)**
    * % Full
    * Liters remaining
    * Zonal distribution of water

* **Pipas de Agua (Water Trucks)**
    * Number of active trucks
    * Total water capacity (in liters) 
    * Zonal distribution

* **Garrafones & Botellas (Large Water Jugs & Bottles)**
    * Number of units distributed 
    * Distribution patterns 

* **Tinacos/Cisternas (Storage Tanks)**
    * Number of buildings with these systems 
    * Average water storage capacity
    * Estimate of the population with access to cisterns

* **Rainfall Data**
    * Historical rainfall patterns (focus on recent years)

* **Desalination**
    * Existing plants (location, capacity)
    * Potential for expansion

* **Rainwater Collection**
    * Potential water collection estimates

* **Zonas Bajo Tandas (Rationed Zones)**
    * Currently affected zones
    * Frequency and severity of rationing 

* **Fugas (Leaks)**
    * Estimated percentage of water loss (40%)
    * Impact on water distribution models 

#QUESTIONS
When using the questions found in data a location should be included. I feel like that can be left out of most of the questions without effecting it. By preappending to the question should make it more dynamic. 

Example: For CDMX, Mexico City and the surrounding area.

Full Example: For CDMX, Mexico City and the surrounding area. What are rainfall patterns (by month/year) and how do they affect water availability?