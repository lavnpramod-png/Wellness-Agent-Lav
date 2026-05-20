
export default function WellnessAgentApp() {
  const meals = [
    {
      title: 'Breakfast',
      meal: 'Moong Dal Chilla + Mint Chutney',
      benefit: 'High protein and easy digestion'
    },
    {
      title: 'Lunch',
      meal: 'Jeera Rice + Vegetable Curry + Buttermilk',
      benefit: 'Gut-friendly and cooling'
    },
    {
      title: 'Dinner',
      meal: 'Khichdi + Curd',
      benefit: 'Light dinner for better sleep'
    }
  ];

  return (
    <div className="min-h-screen bg-gray-100 p-6">
      <div className="max-w-6xl mx-auto">
        <div className="bg-white rounded-3xl shadow-lg p-8 mb-8">
          <h1 className="text-4xl font-bold text-gray-800 mb-2">
            Wellness Agent 🌿
          </h1>
          <p className="text-gray-600 text-lg">
            AI-powered wellness companion for gut health and energy management.
          </p>
        </div>

        <div className="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
          <div className="bg-white rounded-3xl shadow-md p-6">
            <h2 className="text-2xl font-semibold mb-4 text-gray-800">
              Morning Check-In
            </h2>

            <div className="space-y-4">
              <div>
                <label className="block text-gray-700 mb-2">Energy Level</label>
                <input
                  type="range"
                  min="1"
                  max="10"
                  className="w-full"
                />
              </div>

              <div>
                <label className="block text-gray-700 mb-2">Sleep Quality</label>
                <input
                  type="range"
                  min="1"
                  max="10"
                  className="w-full"
                />
              </div>

              <div className="flex items-center gap-3">
                <input type="checkbox" />
                <label className="text-gray-700">Bloating</label>
              </div>

              <div className="flex items-center gap-3">
                <input type="checkbox" />
                <label className="text-gray-700">Acidity</label>
              </div>

              <button className="bg-black text-white px-6 py-3 rounded-2xl mt-4 hover:opacity-90 transition">
                Generate Wellness Plan
              </button>
            </div>
          </div>

          <div className="bg-white rounded-3xl shadow-md p-6">
            <h2 className="text-2xl font-semibold mb-4 text-gray-800">
              Wellness Dashboard
            </h2>

            <div className="space-y-4">
              <div className="bg-gray-50 rounded-2xl p-4">
                <p className="text-gray-500">Gut Health Score</p>
                <h3 className="text-3xl font-bold">82%</h3>
              </div>

              <div className="bg-gray-50 rounded-2xl p-4">
                <p className="text-gray-500">Energy Level</p>
                <h3 className="text-3xl font-bold">7/10</h3>
              </div>

              <div className="bg-gray-50 rounded-2xl p-4">
                <p className="text-gray-500">Hydration</p>
                <h3 className="text-3xl font-bold">2.5L</h3>
              </div>
            </div>
          </div>
        </div>

        <div className="bg-white rounded-3xl shadow-lg p-8">
          <h2 className="text-3xl font-bold text-gray-800 mb-6">
            AI Meal Recommendations
          </h2>

          <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
            {meals.map((meal, index) => (
              <div
                key={index}
                className="bg-gray-50 rounded-2xl p-6 border border-gray-200"
              >
                <h3 className="text-xl font-semibold mb-3 text-gray-800">
                  {meal.title}
                </h3>

                <p className="text-lg font-medium mb-3 text-gray-700">
                  {meal.meal}
                </p>

                <p className="text-gray-500 text-sm">
                  {meal.benefit}
                </p>
              </div>
            ))}
          </div>
        </div>
      </div>
    </div>
  );
}
